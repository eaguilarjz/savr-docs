---
title: Security
parent: English
nav_order: 9
---

> 🌐 Lee esta página en [Español](../../es/security/)

# Security

This page covers everything related to keeping your savr account secure: passwords, two-factor authentication, recovery codes, and sessions.

You'll find these settings under **Profile → Security**.

---

## Change your password

1. Open **Profile** and find the **Security** section.
2. Click **Change password**.
3. Enter your **current password**, then a **new password** (8 characters minimum), and confirm.
4. Click **Save**.

Once changed, every signed-in session continues to work, but any signed-out session will require the new password.

> **Tip:** Use a password manager. The strongest password is one you don't have to remember.

---

## Two-Factor Authentication (MFA)

Two-factor authentication adds a second step to sign-in: even if someone learns your password, they can't get in without a code from an authenticator app on your phone. Enabling MFA is the single biggest improvement you can make to account security.

savr supports **TOTP** (time-based one-time passwords) — the same standard used by Google Authenticator, Authy, 1Password, Bitwarden, and most modern password managers.

### Set up MFA

1. Open **Profile → Security** and click **Enable two-factor authentication**.
2. A modal walks you through three steps:

   **Step 1 — Scan the QR code**
   - Open your authenticator app (Google Authenticator, Authy, 1Password, Bitwarden, etc.).
   - Add a new account by scanning the QR code shown on screen.
   - If you can't scan, click **Show secret** and enter the 32-character key manually.

   **Step 2 — Verify**
   - Type the 6-digit code currently shown in your authenticator.
   - Click **Verify**.

   **Step 3 — Save your recovery codes**
   - savr generates **8 recovery codes**.
   - **Download** them as a `.txt` file or copy them to your password manager.
   - These codes are your fallback if you lose access to your authenticator. Keep them somewhere you'll find again — but not on the same device as your authenticator.

3. Click **Done**. MFA is now active on your account.

### Sign in with MFA

After entering your email and password on the sign-in page, savr asks for a second factor:

- Open your authenticator app and enter the current 6-digit code, **or**
- Click **Use a recovery code** and enter one of the codes you saved during setup.

The 6-digit codes refresh every 30 seconds. If a code is rejected, wait for the next one and try again — the most common cause is the previous code having expired.

### Recovery codes

Each recovery code is **single-use**. Once used, that code can't be used again.

- You receive **8 codes at setup**.
- Use them only when you don't have access to your authenticator (lost phone, switched devices without migrating codes, app deleted by mistake).
- If you've used most of them and want fresh codes, regenerate them from **Profile → Security → Regenerate recovery codes**. Regenerating invalidates the old set.

> **Treat recovery codes like a backup key.** If someone has your codes and your password, they have full access. Store them in a password manager or somewhere physically secure.

### What if I lose my phone *and* my recovery codes?

If both are gone, you'll need to contact support to verify your identity and recover access. This is a manual process, intentionally — it's the safety net that prevents an attacker from social-engineering their way back in.

This is also why we recommend keeping recovery codes in a separate location from your phone (e.g. a password manager that's not synced to that phone, or a printed copy in a safe).

### Disable MFA

1. Open **Profile → Security** and click **Disable two-factor authentication**.
2. Enter your password to confirm.
3. MFA is removed from your account.

You can re-enable it any time. New recovery codes are generated each time you set up MFA from scratch — old codes are not preserved.

---

## Sessions

When you sign in to savr, your session is held in two secure cookies:

| Cookie | Lifetime | Purpose |
|---|---|---|
| **Access token** | 15 minutes | Used for every request |
| **Refresh token** | 30 days | Issues a new access token automatically when the access token expires |

Both cookies are HTTP-only (so JavaScript on the page can't read them) and SameSite=strict (so they aren't sent in cross-site requests). In production, both cookies are also marked Secure (HTTPS-only).

In practice this means:

- You stay signed in across browser restarts for up to 30 days.
- Idle for a long time? You'll be signed out silently if your refresh token expires while you weren't using the app.
- **Sign out** clears both cookies on this device.

### Multiple devices

You can be signed in on multiple devices at once — each device has its own pair of cookies. Signing out on one device doesn't sign you out on others. There's no "active sessions" list to view at the moment.

---

## Rate limits

To protect your account from brute-force attacks, certain endpoints are rate-limited:

| Action | Limit |
|---|---|
| Sign in / MFA verification | 10 attempts per 15 minutes |
| Registration | 10 per 15 minutes |
| Forgot password | 3 requests per hour |

If you hit a limit, you'll see an error asking you to wait. Limits reset automatically.

---

## Best practices

- **Enable MFA.** Almost every account compromise starts with a stolen or reused password. MFA defeats this.
- **Use a password manager.** Generate a unique, long password for savr and let your password manager remember it.
- **Save recovery codes somewhere you can actually find them.** A password manager entry, a paper copy in a safe, or both.
- **Don't store recovery codes on the same device as your authenticator.** If you lose the device, you've lost both.
- **Sign out on shared devices.** Don't rely on the "remember me" cookie if anyone else uses that browser.
