---
title: Accounts
parent: English
nav_order: 3
---

> {% include lang-globe.html %} Lee esta página en [Español](../../es/accounts/)

# Accounts

Accounts in savr mirror the real-world places your money lives: bank accounts, credit cards, the cash in your wallet, your investment portfolio, the loan that's slowly shrinking. Each transaction belongs to an account, and every account's balance updates the moment you record activity — so the totals you see in savr stay in sync with reality.

Set them up once. Maintain them with two minutes a week.

---

## Account types

savr supports six types. The type matters because it controls how the account is grouped on the page, how its balance is interpreted, and which features show up.

| Type | Use it for | Notes |
|---|---|---|
| **Checking** | Day-to-day spending | Where most transactions live |
| **Savings** | Money set aside | Treated like checking for budgeting purposes |
| **Credit Card** | Credit cards | Spending here doesn't reduce a cash account; record payments as Transfers |
| **Cash** | Physical cash on hand | Pocket money, that envelope in the drawer |
| **Investment** | Brokerage, retirement, crypto | Tracks the balance; not designed for trade-by-trade detail |
| **Loan** | Mortgages, auto loans, personal loans, student loans | Interest rate, monthly payment, linked payment category |

> Loans are special — see [Loan accounts](#loan-accounts) below for the full treatment.

---

## Add an account

1. Open **Accounts** and click **Add Account**.
2. Enter:
   - **Name** — how it shows up everywhere in savr (e.g. "Chase Checking")
   - **Type** — pick one of the six
   - **Opening balance** — what's in the account right now
3. For loans, fill in the loan-specific fields.
4. Click **Save**.

savr automatically creates an **Opening Balance** transaction equal to your starting amount. It marks this transaction specially: it sets the account balance but doesn't affect your budget or category spending.

> **For example:** You added a checking account with an opening balance of $2,847.13. savr creates a single transaction dated today, marked as Opening Balance, with that amount. Your account shows $2,847.13. Your budget is unaffected — that money just exists, ready to be allocated.

---

## Loan accounts

Loan accounts are where savr earns its keep. They give you a place to track the principal balance, the interest rate, and the payment so the math stays honest each month.

When creating or editing a loan, you can set:

| Field | Meaning |
|---|---|
| **Interest rate** | Annual percentage rate. Used in reports and recurring debt payments. |
| **Monthly payment** | The expected periodic payment — used as a default when you record payments. |
| **Linked payment category** | The category where loan interest and fees post when you record a payment. |

When you create a loan, you can either link to an **existing category** or have savr **create a new category** for it (and optionally place that category in a new group, like "Debt"). Either way, interest charges land in your budget like any other expense — visible, real, planned for.

For how to record loan payments with separate principal, interest, and fees amounts, see [Debt payments](../transactions/#debt-payments). For monthly payments that fire on schedule, see [Recurring debt payments](../recurring/#recurring-debt-payments).

> **Pro tip:** When the loan is paid off, [close the account](#close-an-account) instead of deleting it. The history is part of your story — you'll want to look back and see the day that mortgage hit zero.

---

## Edit, close, reopen, delete

### Edit an account

Click the account row to open its editor. You can change:

- The name
- The type
- (For loans) the interest rate and monthly payment

Opening balance is set at creation. To adjust historical balances, edit or add a transaction directly.

### Close an account

When you're done with an account but want to keep its history:

1. Open the account's detail view.
2. Click **Close**.

Closed accounts are hidden from the main accounts list and don't appear in transaction selectors, but every transaction stays put. This is the right move for paid-off credit cards, sold investments, and accounts at banks you no longer use.

### Reopen an account

In the closed accounts section of the Accounts page, click **Reopen**. Everything comes back exactly as you left it.

### Delete an account

You can permanently delete an account only if it has no transactions other than its opening balance. If you need to delete an account with activity, you've got two options:

1. Delete or reassign every transaction first, or
2. Close the account instead — closing preserves history.

Closing is almost always what you want. Deletion is for when you created an account by mistake.

---

## Reconciliation

Each account has a **Reconcile** button that walks you through matching savr to your bank's statement. This is the move that catches typos, missed transactions, and the occasional double-charge from your bank.

If your account balance in savr starts to drift from reality, run a reconciliation. It's the cleanest way to catch up.

→ Full guide: [Reconciliation](../reconcile/)

---

## CSV import

Got a year of transactions sitting in a CSV from your bank? Don't type them all in. savr has a three-step import wizard that handles the gnarly stuff (date formats, sign conventions, header mapping) for you.

→ Full guide: [Import & Export](../import-export/)

---

## Organizing the accounts page

### Grouping by type

Accounts are automatically grouped by type. Each group (Checking, Savings, Credit Card, etc.) has a header that shows the type's total balance — useful for "how much cash do I actually have right now?" at a glance.

### Collapse and expand

Click any group header to collapse it. Use this to focus on the accounts you're actively working with. The closed loans and the credit cards you barely touch don't need to clutter your view.

### Reorder accounts

savr supports drag-and-drop on two levels:

- **Within a group** — drag individual accounts to change their order
- **Across groups** — drag the group header to change the order of types

Your ordering saves automatically and persists across sessions.

> **For example:** You have three checking accounts and you always think of "Chase Checking" first. Drag it to the top of the Checking group. Now it's always first when you record a transaction.

---

## Account detail view

Click an account's name to open its detail page. You'll see:

- The current balance and account metadata (type, opening balance, created date)
- All transactions for this account, with the same filters as the main Transactions page
- A **New Transaction** button to record activity directly against this account
- A **Reconcile** button to match against a statement
- An **Import CSV** option to bulk-add transactions

This is the fastest way to reconcile against a paper or online statement, or to add a streak of transactions for one account in a row.

---

## Account balances explained

Balances are stored to two decimal places. Every time you create, update, or delete a transaction, the affected account's balance recalculates atomically — so the number on the Accounts page always matches the sum of its activity. No drift, no "let me close and reopen the app to refresh."

Transfers between two accounts post a paired entry: one debit, one credit. Both accounts update together.

For credit card accounts, the balance reflects what you owe. A positive balance means you have an outstanding amount to pay. When you record a payment, transfer money from a checking account to the credit card account — the credit card balance goes down, the checking balance goes down, and your overall net worth is unchanged.

> **Common scenario:** Your Chase Sapphire shows a balance of $843.21. You pay it off by transferring $843.21 from Checking. Now Sapphire shows $0 and Checking shows $843.21 less. The transfer is one savr action, two linked transactions, zero math on your end.
