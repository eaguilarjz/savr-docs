---
title: Security
parent: English
nav_order: 13
---

> {% include lang-globe.html %} Lee esta página en [Español](../../es/security/)

# Security

Your savr account contains a comprehensive picture of your finances. We take that seriously, and you should too.

This page covers everything you can do to keep your account secure: passwords, two-factor authentication, recovery codes, and how sessions work. Most of it is two-minute one-time setup that pays off forever.

You'll find these settings under **Profile → Security**.

---

## How you sign in

savr accepts three ways to sign in. You can use any one of them, or mix and match — they all reach the same account.

| Method | What you need | Notes |
|---|---|---|
| **Email + password** | Your email address and your savr password | The classic. Pair with [MFA](#two-factor-authentication-mfa) for the strongest setup. |
| **Sign in with Google** | A Google account whose email matches yours in savr | One click. No password to remember. |
| **Sign in with Microsoft** | A Microsoft account (personal or work) whose email matches yours in savr | Same idea — one click. |

### How OAuth sign-up works

When you click **Sign in with Google** or **Sign in with Microsoft** on the sign-up screen, savr:

1. Sends you to the provider to confirm.
2. Reads the email address from the response.
3. **Creates a new account** with that email, or **links** the provider to your existing savr account if the email already exists. No duplicate accounts.

### Switching methods later

You're not locked into the method you started with. From **Profile → Security → Connected accounts**, you can:

- Add Google or Microsoft to an email/password account (now you have both options at sign-in).
- Remove Google or Microsoft from an account that has at least one other way in.
- An account with **only OAuth** (no password) can't unlink its last provider — set a password first via **Forgot password?**, then come back and unlink.

---

## Change your password

1. Open **Profile** and find the **Security** section.
2. Click **Change password**.
3. Enter your **current password**, then a **new password** (8 characters minimum), and confirm.
4. Click **Save**.

Once changed, every signed-in session continues to work, but any signed-out session (a different device, an old browser) will require the new password.

> **Pro tip:** Use a password manager. The strongest password is one you don't have to remember — long, random, unique to savr. 1Password, Bitwarden, Apple's iCloud Keychain, your browser's built-in manager: all fine. Pick one and let it do its job.

---

## Connected accounts

The **Connected accounts** section lists every external sign-in method linked to your savr account — Google, Microsoft, and any future providers.

### Add a provider

1. Open **Profile → Security → Connected accounts**.
2. Click **Connect** next to the provider.
3. You're handed off to Google/Microsoft to confirm. Once you're back, the provider is listed with the email address it used.

After connecting, the provider becomes another way to sign in. Useful if you want a fast click-through option *and* a password as backup.

### Remove a provider

Click **Disconnect** next to a provider in the list. The change is immediate — no confirmation dialog.

The one exception: if the provider you're removing is the **only** way you can sign in (an OAuth-only account with no password), savr won't let you. Set a password first via **Forgot password?** on the sign-in page, then come back to remove the provider.

> **Why connect more than one?** Redundancy. If you lose access to one provider account, the other still works. Pair this with [Recovery codes](#recovery-codes) and you've got real account-recovery resilience.

---

## Two-Factor Authentication (MFA)

Two-factor authentication adds a second step to sign-in: even if someone learns your password, they can't get in without a code from an authenticator app on your phone. Enabling MFA is the single biggest improvement you can make to account security.

savr supports **TOTP** (time-based one-time passwords) — the same standard used by Google Authenticator, Authy, 1Password, Bitwarden, and most modern password managers.

### Set up MFA

1. Open **Profile → Security** and click **Enable two-factor authentication**.
2. A modal walks you through three steps:

   **Step 1 — Scan the QR code**
   - Open your authenticator app.
   - Add a new account by scanning the QR code on screen.
   - If you can't scan, click **Show secret** and enter the 32-character key manually.

   **Step 2 — Verify**
   - Type the 6-digit code currently shown in your authenticator.
   - Click **Verify**.

   **Step 3 — Save your recovery codes**
   - savr generates **8 recovery codes**.
   - **Download** them as a `.txt` file or copy them to your password manager.
   - These codes are your fallback if you lose access to your authenticator. Keep them somewhere you'll find again — but **not on the same device as your authenticator**.

3. Click **Done**. MFA is now active.

> **The five-minute setup that pays off forever.** Most account compromises start with a stolen or reused password. MFA neutralizes the attack. The whole setup is under five minutes. Just do it.

### Sign in with MFA

After entering your email and password on the sign-in page, savr asks for a second factor:

- Open your authenticator app and enter the current 6-digit code, **or**
- Click **Use a recovery code** and enter one of the codes you saved during setup.

The 6-digit codes refresh every 30 seconds. If a code is rejected, wait for the next one and try again — the most common cause is the previous code having expired between you reading it and typing it.

### Trusted devices

The MFA prompt has a **Trust this device for 30 days** checkbox. Tick it, and that device skips the MFA step on every sign-in for the next 30 days. After 30 days, the trust expires and you're back to entering codes.

A few things worth knowing:

- **Trust is per-device, per-browser.** Trusting your laptop in Chrome doesn't trust your phone or your laptop in Firefox.
- **It's a cookie.** If you clear cookies, the trust is gone — that's a feature, not a bug.
- **Don't tick it on shared computers.** That's the whole reason MFA exists. Use trusted devices only on phones, laptops, and tablets that nobody else touches.
- **You're still asked for password + 6-digit code on the first sign-in.** Trust kicks in starting on the next visit.

> **Recommendation:** Trust the two or three devices you actually use. Leave the box unchecked everywhere else. You'll only see the MFA prompt occasionally — when the 30 days roll over, when a cookie clears, or when you sign in somewhere new.

### Recovery codes

Each recovery code is **single-use**. Once used, that code can't be used again.

- You receive **8 codes at setup**.
- Use them when you don't have access to your authenticator (lost phone, switched devices without migrating codes, app deleted by mistake).
- If you've used most of them and want fresh codes, regenerate them from **Profile → Security → Regenerate recovery codes**. Regenerating invalidates the old set.

> **Treat recovery codes like a backup key.** If someone has your codes and your password, they have full access. Store them in a password manager or somewhere physically secure (like a printed copy in a safe). Don't email them to yourself.

### What if I lose my phone *and* my recovery codes?

If both are gone, contact support to verify your identity and recover access. This is intentionally manual — it's the safety net that prevents someone from social-engineering their way back into your account.

The fix for this scenario is to never get into it: keep recovery codes somewhere separate from your phone. A password manager that's not synced to that phone, or a printed copy in a drawer, both work.

### Disable MFA

1. Open **Profile → Security** and click **Disable two-factor authentication**.
2. Enter your password to confirm.
3. MFA is removed from your account.

You can re-enable it any time. New recovery codes are generated each time you set up MFA from scratch — old codes don't carry over.

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
- Idle for a long time? You'll be signed out silently if your refresh token expires while you weren't using the app. No drama; just sign in again.
- **Sign out** clears both cookies on this device.

### Multiple devices

You can be signed in on multiple devices at once — each device has its own pair of cookies. Signing out on one device doesn't sign you out on the others.

> **For example:** You're signed in on your laptop and your phone. You hand the phone to a friend (who doesn't see savr — they're using a different app), then sign out on the laptop. Your phone session is unaffected.

There's no "active sessions" list yet. If you ever lose a device and want to make absolutely sure all sessions are killed, change your password — it doesn't invalidate existing sessions, but new ones will require the new password.

---

## Rate limits

To protect your account from brute-force attacks, certain endpoints are rate-limited:

| Action | Limit |
|---|---|
| Sign in / MFA verification | 10 attempts per 15 minutes |
| Registration | 10 per 15 minutes |
| Forgot password | 3 requests per hour |

If you hit a limit, you'll see an error asking you to wait. Limits reset automatically.

Most users will never see one of these messages. They exist to slow down attackers who'd otherwise try thousands of password guesses against your account.

---

## Best practices

A short list, in order of importance:

1. **Enable MFA.** Almost every account compromise starts with a stolen or reused password. MFA defeats this. (Two minutes. Just do it.)
2. **Use a password manager.** Generate a unique, long password for savr and let your password manager remember it. Don't reuse a password from another site.
3. **Save recovery codes somewhere you can actually find them.** A password manager entry, a paper copy in a safe, or both. Don't put them in an email or in a Notes app on the same device as your authenticator.
4. **Don't store recovery codes on the same device as your authenticator.** If you lose the device, you've lost both — and you lose the safety net.
5. **Sign out on shared devices.** Don't rely on the "remember me" cookie if anyone else uses that browser.
6. **Treat the trial-end and renewal emails as security checkpoints too.** They confirm your email is still working and your account is still active. If you stop receiving expected emails from savr, check your spam folder and consider whether your email account has been compromised.

You'll never regret these. You might regret skipping them.
