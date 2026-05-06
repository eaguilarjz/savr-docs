---
title: Transactions
parent: English
nav_order: 4
---

> 🌐 Lee esta página en [Español](../es/transactions/)

# Transactions

Transactions record every movement of money in and out of your accounts. They drive everything else in savr: account balances, category spending, and budget metrics.

You can manage transactions from the **Transactions** page or directly from any account's detail view.

---

## Transaction types

savr supports four transaction types. Picking the right one matters because it affects both account balances and budget calculations.

| Type | Effect on account | Effect on budget |
|---|---|---|
| **Income** | Adds money to the account | Increases **To Be Budgeted** |
| **Expense** | Removes money from the account | Increases **Spent** in the chosen category |
| **Transfer** | Moves money between two of your accounts | No effect on budget — money stays inside your net worth |
| **Credit** (refund) | Adds money back to the account | **Reduces** Spent in the chosen category. Does **not** add to TBB. |

> **Why Credit and Income are different:** A refund cancels out a previous expense — your category should reflect the net cost, but the refund isn't new income. Credit handles this correctly. Use Income for actual new money: paychecks, gifts, interest earned.

---

## Create a transaction

1. Open **Transactions** and click **New Transaction** (or open an account's detail page and use the same button there).
2. Fill in:
   - **Type** — Income, Expense, Transfer, or Credit
   - **Account** — which account this affects
   - **Amount** — always positive; the type determines direction
   - **Date** — defaults to today
   - **Category** — required for Expense and Credit
   - **Payee** — optional, but useful for spending analysis
   - **Memo** — optional notes
   - **Cleared** — toggle if the transaction has cleared your bank statement
3. Click **Save**.

### Transfers

For a Transfer, you'll be asked for both the **from** account and the **to** account. savr creates a linked pair of transactions — one debit and one credit — that always move together. If you edit or delete one side, the other follows.

---

## Splits

A split lets you divide a single transaction across multiple categories. This is especially useful for grocery store runs that include both food and household items, or any other purchase that doesn't fit cleanly into one category.

To split a transaction:

1. In the create or edit dialog, toggle **Split**.
2. Add a split row for each category. Each row has:
   - **Category**
   - **Amount**
   - **Memo** (optional)
3. The total of the splits must match the transaction's total amount.

You can have as many splits as you need. To remove a split, delete its row — if only one split remains, savr converts the transaction back to a normal (non-split) transaction.

---

## Debt payments

Debt payments are a specialized transaction type for recording payments against a loan account. They give you a clean breakdown of the three things a loan payment usually includes:

| Component | Where it goes |
|---|---|
| **Principal** | Reduces the loan account's balance |
| **Interest** | Posts as an expense to the linked payment category |
| **Fees** | Posts as an expense to the linked payment category |

To record a debt payment:

1. Open **New Transaction** and switch to **Debt Payment** mode.
2. Pick the **source account** (where the money comes from — usually checking).
3. Pick the **loan account** being paid down.
4. Enter the **principal**, **interest**, and **fees** amounts.
5. Confirm the payment category (defaults to the one linked to the loan).
6. Save.

Your checking balance drops by the total payment, the loan balance drops by the principal, and interest plus fees show up as spending in the payment category.

---

## Cleared status

Each transaction has a **cleared** flag. Use it to mark transactions that have been confirmed by your bank.

Common workflows:

- Reconcile against a statement once a month, marking each line cleared as you go.
- Leave recently entered transactions uncleared until they post on your bank's side.

The cleared flag is informational — it doesn't change balance calculations.

---

## Edit and delete transactions

Click any transaction in the list to open its edit dialog. You can change any field, including converting a regular transaction into a split or back. Click **Save** to apply.

To remove a transaction, open the edit dialog and click **Delete**. Deletes are permanent and the affected account's balance updates immediately.

> **Opening balance transactions** are special. They're auto-created with each account and don't affect budgets. You can edit the amount if you mistyped your starting balance, but you can't delete the opening balance entry without deleting the account.

---

## Filters

The Transactions page has a filter bar across the top so you can find activity quickly:

| Filter | What it does |
|---|---|
| **Account** | Show transactions in one specific account |
| **Category** | Show transactions in a specific category |
| **Payee** | Show transactions with a specific payee |
| **Type** | Restrict to Income, Expense, Transfer, or Credit |
| **Date range** | Pick a start and end date |

Filters combine with **AND** logic — every constraint applies. To clear filters, hit the reset button or remove them individually.

---

## Pagination

Long transaction lists load in pages of 50 at a time. As you scroll near the bottom, savr fetches the next batch automatically. There's no "next page" button — just keep scrolling.

For very large queries, you may want to apply a date range filter rather than scrolling through everything.

---

## Recurring transaction links

Transactions created from a [recurring rule](recurring/) keep a reference to the rule that produced them. This lets you trace a transaction back to its template, and lets savr keep your recurring schedule accurate.

Edits to a transaction created by a recurring rule don't change the rule itself — only that one occurrence.

---

## Account detail view

Every account has a detail page that shows the same transaction list, scoped to just that account. Use it to:

- Reconcile against a paper or online statement
- Quickly add multiple transactions for one account in a row
- Review activity over a specific period without setting account filters
