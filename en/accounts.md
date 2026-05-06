---
title: Accounts
parent: English
nav_order: 3
---

> 🌐 Lee esta página en [Español](../es/accounts/)

# Accounts

Accounts represent the real financial accounts you want to track in savr: bank accounts, credit cards, cash on hand, investment accounts, and loans.

Every transaction belongs to an account. Account balances update automatically as you record activity, so the totals you see in savr stay in sync with reality.

---

## Account types

savr supports six account types. Choosing the right type matters because it affects how the account is grouped, how its balance is interpreted, and which features apply to it.

| Type | Use it for | Notes |
|---|---|---|
| **Checking** | Day-to-day spending accounts | Most transactions live here |
| **Savings** | Money set aside | Treated like checking for budgeting purposes |
| **Credit Card** | Credit cards | Spending here doesn't reduce a cash account; use Transfer to record payments |
| **Cash** | Physical cash on hand | Useful for tracking pocket money |
| **Investment** | Brokerage, retirement, crypto | Track balances; not designed for trade-by-trade detail |
| **Loan** | Mortgages, auto loans, personal loans, student loans | Includes interest rate, monthly payment, and a linked payment category |

> Loans are special — see [Loan accounts](#loan-accounts) below.

---

## Add an account

1. Open **Accounts** and click **Add Account**.
2. Enter:
   - **Name** — how the account appears throughout savr (e.g. "Chase Checking")
   - **Type** — pick from the six options above
   - **Opening balance** — the balance right now. savr uses this to seed the account.
3. For loans, fill in the loan-specific fields (see below).
4. Click **Save**.

savr automatically creates an **Opening Balance** transaction equal to the value you entered. This transaction is marked specially: it sets the account balance but doesn't affect your budget or category spending.

---

## Loan accounts

Loan accounts have a few extra fields and features so you can track principal, interest, and progress over time.

When creating or editing a loan, you can set:

| Field | Meaning |
|---|---|
| **Interest rate** | Annual percentage rate. Used for reporting and recurring debt payments. |
| **Monthly payment** | The expected periodic payment. Used as a default when applying recurring payments. |
| **Linked payment category** | The category that loan interest and fees post to when you record a payment. |

When creating a loan, you can either link to an **existing category** or have savr **create a new category** for it (and optionally place it in a new group, like "Debt"). This keeps interest charges visible in your budget without manual setup.

For how to record loan payments with separate principal, interest, and fees amounts, see [Debt payments](../transactions/#debt-payments).

---

## Edit, close, reopen, delete

### Edit an account

Click the account row to open its editor. You can change the name, type, and (for loans) the interest rate and monthly payment. Opening balance is set at creation — to adjust historical balances, edit or add a transaction.

### Close an account

When you're done using an account but want to keep its history:

1. Open the account's detail view.
2. Click **Close**.

Closed accounts are hidden from the main accounts list and don't appear in transaction selectors, but every transaction stays put. This is the right move for paid-off credit cards, sold investments, and accounts you've left behind.

### Reopen an account

In the closed accounts section of the Accounts page, click **Reopen** to bring it back. All history is preserved.

### Delete an account

You can permanently delete an account only if it has no transactions other than its opening balance. If you need to delete an account with activity, you have two options:

1. Delete or reassign every transaction first, or
2. Close the account instead — closing preserves history.

---

## Organizing the accounts page

### Grouping by type

Accounts are automatically grouped by type. Each group (Checking, Savings, Credit Card, etc.) has a header that shows the type's total balance.

### Collapse and expand

Click any group header to collapse it. Use this to focus on the accounts you're actively working with.

### Reorder accounts

savr supports drag-and-drop on two levels:

- **Within a group** — drag individual accounts to change their order.
- **Across groups** — drag the group header to change the order in which types are displayed.

Your ordering is saved automatically and persists across sessions.

---

## Account detail view

Click an account name to open its detail page. You'll see:

- The current balance and account metadata (type, opening balance, created date)
- All transactions for this account, with the same filters available on the main Transactions page
- A **New Transaction** button so you can record activity directly against the account

This is the fastest way to reconcile an account against a paper or online statement.

---

## Account balances explained

Balances are stored to two decimal places. Every time you create, update, or delete a transaction, the affected account balance recalculates atomically — so the number on the Accounts page always matches the sum of its activity.

Transfers between two accounts post a paired entry: one debit, one credit. Both accounts update together.

For credit card accounts, the balance reflects what you owe (a positive number means a balance is outstanding). When you record a payment, transfer money from a checking account to the credit card account — the credit card balance goes down, the checking balance goes down, and your overall net worth is unchanged.
