---
title: Reconciliation
parent: English
nav_order: 9
---

> 🌐 Lee esta página en [Español](../../es/reconcile/)

# Reconciliation

Reconciliation is the act of saying: "savr's record of this account matches reality."

You take your bank statement (or your bank's online "current balance"), compare it to what savr thinks the balance should be, and sort out any differences. When the math agrees, you mark it reconciled and move on with your life.

If you've never reconciled before — don't be intimidated. savr does almost all of the work. You're just clicking checkboxes until two numbers match.

---

## Why reconcile

Three reasons:

1. **Catch your own typos.** You wrote $51 instead of $15. It happens. Reconciliation surfaces these the moment they break the math.
2. **Catch your bank's mistakes.** Rare but real. A duplicate charge, a missed credit, a fee you didn't know about — these show up when savr's number disagrees with your bank's.
3. **Build trust in your own data.** When the balance in savr is the actual balance in your account, you stop hedging your decisions with "well, give or take a few hundred."

The reward for spending two minutes a month per account is total confidence in every number you see in savr.

---

## How to reconcile

1. Open the **Accounts** page and click the account you want to reconcile.
2. On the account detail page, click **Reconcile**.
3. You're now on the reconciliation page. Three things to do:

### Step 1 — Enter the statement

At the top:

- **Statement date** — the date on the bank statement (or just today, if you're using a real-time online balance)
- **Statement balance** — the balance your bank says the account had on that date

Enter both. savr stores them when you finish.

### Step 2 — Clear the matching transactions

Below, savr shows you a table of every unreconciled transaction in the account. Click rows (or use the checkboxes) to mark which ones appear on the statement.

As you click, three numbers update at the bottom of the page:

| Number | What it is |
|---|---|
| **Cleared Balance** | What savr thinks your balance should be after all the transactions you've checked |
| **Statement Balance** | What you typed at the top |
| **Difference** | Statement Balance − Cleared Balance |

When **Difference = $0** (or within half a cent), the **Finish** button activates.

### Step 3 — Finish

Click **Finish**. savr:

- Marks every checked transaction as cleared and reconciled
- Records the reconciliation date and statement balance
- Returns you to the account detail page

Done. The account is now reconciled.

---

## What if it doesn't balance?

This is the part that makes reconciliation feel scary. It's actually the part where it earns its keep.

If the **Difference** isn't zero, something is wrong. Either:

- A transaction is in your statement but not in savr (missing transaction)
- A transaction is in savr but not on the statement (extra transaction, or wrong account)
- A transaction has the wrong amount somewhere

savr doesn't auto-suggest where the issue is — that's a problem only you can solve, because it depends on what's on your statement. But here's the workflow:

1. **Look at the size of the difference.** If it's $43.21, you're probably looking for a single transaction worth $43.21.
2. **Scan your statement for transactions you haven't checked off.** Anything on the statement but not on your screen? That's a missing transaction. Add it (open a new tab and use the Transactions page) and come back.
3. **Scan your checked transactions for ones not on the statement.** Anything checked but not on the statement? Either it hasn't posted yet (uncheck it and try again next month) or it doesn't belong here (delete it or fix it).
4. **Watch for sign errors and amount typos.** A $51 charge entered as $15 will produce a $36 difference. A debit entered as a credit will produce a difference equal to twice the amount (because it's wrong by both -$X and +$X).

> **Common scenario:** You expected the reconciliation to balance and it's off by $25. Looking at the bank statement, you spot a $25 ATM withdrawal you forgot to enter into savr. Open a new tab, add the transaction, return to the reconciliation page (it'll be there waiting), check the new transaction, and the difference goes to zero. Click Finish.

---

## How often to reconcile

Two reasonable cadences:

- **Monthly**, against the bank's official statement. Old-school but rock-solid. The statement is authoritative.
- **Weekly or biweekly**, against the bank's online "current balance." Faster feedback, fewer transactions per session, smaller problems if something's off.

Pick whatever you'll actually do. A monthly habit you keep beats a weekly habit you don't.

> **Pro tip:** Set a recurring calendar reminder for the day after your statement period ends. "Reconcile checking" — five minutes max. Future-you will thank present-you.

---

## Reconciling specific account types

### Checking and savings

The bread and butter of reconciliation. Run it monthly against the statement. Most months it balances on the first try in under five minutes.

### Credit cards

Same flow as checking. Note that the balance on a credit card is what you owe (a positive number). The statement balance from the credit card company is what they're billing you for that period — which may not match your current balance, since you've kept spending after the statement date. Match against the statement balance for the period it covers, ignoring transactions that happened after.

### Cash

Cash is a pain to reconcile because there's no statement. Best practice: count the cash in your wallet, enter that as the statement balance, and check off all the transactions that are in savr. If it doesn't balance, you forgot to record a coffee somewhere. Add it, finish, move on.

### Investment accounts

Investment balances move daily based on market value. Reconciling them against a statement is mostly about confirming deposits and withdrawals — the market-driven changes are messy to capture transaction by transaction. Many people just update the opening balance once a quarter and don't bother with full reconciliation.

### Loans

Loans typically have just one transaction a month (the payment) plus interest accrual. If you're using [debt payment](../transactions/#debt-payments) transactions, the balance should track your lender's statement closely. Run a reconciliation when the lender sends a year-end statement, or whenever the numbers feel off.

---

## Reconciliation history

Each reconciliation is recorded against the account, including the statement date, balance, and which transactions were cleared. Future reconciliations build on top — the "previous statement balance" shown on the reconciliation page is the last finished one.

You don't need to look at history often. It's just there for the record.

---

## Tips

- **Reconcile one account at a time.** Don't try to reconcile checking and savings simultaneously — finish one before starting the other.
- **Don't force a balance.** If the difference is $0.34 and you can't find it, do not just click Finish anyway. The reconciliation flow won't even let you (Finish is disabled until the difference is zero) — and that's a feature. Find the actual issue. It's almost always a real transaction that needs to be added or corrected.
- **A failed reconciliation is information.** If you can't get to zero, savr is telling you "your records and reality are out of sync somewhere." That's a problem worth fixing now, not ignoring.
- **The first time is the hardest.** If you're starting reconciliation on an account that hasn't been reconciled in a year, it'll take longer than five minutes. That's normal. After the first one, it's quick.
