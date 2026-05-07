---
title: Transactions
parent: English
nav_order: 4
---

> 🌐 Lee esta página en [Español](../../es/transactions/)

# Transactions

Transactions are the receipts of your financial life. Every dollar that moves — in, out, or sideways between your own accounts — gets a transaction.

savr uses transactions to drive everything else: account balances, category spending, the budget, the reports. Get these right and the rest takes care of itself.

You can manage transactions from the **Transactions** page or directly from any account's detail view. Both work the same way.

---

## The four transaction types

Picking the right type matters. Here's the cheat sheet:

| Type | Effect on account | Effect on budget |
|---|---|---|
| **Income** | Adds money to the account | Increases **To Be Budgeted** |
| **Expense** | Removes money from the account | Increases **Spent** in the chosen category |
| **Transfer** | Moves money between two of your accounts | No effect — money stays inside your net worth |
| **Credit** (refund) | Adds money back to the account | **Reduces** Spent in the chosen category. Does **not** add to TBB. |

> **Why Credit and Income are different:** A refund cancels a previous expense. Your category should reflect the net cost (the $80 grocery bill minus the $20 you returned), not "$80 spent + $20 of new income to budget." Credit gets this right. Use Income for actual new money: paychecks, gifts, interest earned.

### Quick examples

| You did this | Use this type |
|---|---|
| Got paid by your employer | Income |
| Bought groceries | Expense |
| Returned a $30 shirt | Credit (against your Clothing category) |
| Paid off your credit card from checking | Transfer |
| Got a $50 birthday check from grandma | Income |
| Got a refund for a canceled flight | Credit (against your Travel category) |

---

## Create a transaction

1. Open **Transactions** and click **New Transaction** (or hit the same button on an account's detail page).
2. Fill in:
   - **Type** — Income, Expense, Transfer, or Credit
   - **Account** — which account this affects
   - **Amount** — always positive; the type tells savr the direction
   - **Date** — defaults to today
   - **Category** — required for Expense and Credit
   - **Payee** — optional, but useful for spending analysis
   - **Memo** — optional notes
   - **Cleared** — toggle if it's already cleared your bank statement
3. Click **Save**.

### Transfers

For a Transfer, savr asks for both the **from** account and the **to** account. It creates a linked pair of transactions — one debit, one credit — that always move together. Edit one, the other updates. Delete one, the other goes too.

> **For example:** You move $500 from Checking to Savings. savr records:
> - Checking: -$500 (Transfer to Savings)
> - Savings: +$500 (Transfer from Checking)
> 
> Both transactions share an internal pairing. Your net worth doesn't change; your Checking balance dropped, your Savings balance grew.

---

## Splits

A split lets you divide one transaction across multiple categories. This is the move for grocery store runs that include both food and household items, or any other purchase that doesn't fit cleanly in one bucket.

To split:

1. In the create or edit dialog, toggle **Split**.
2. Add a row for each category, each with:
   - **Category**
   - **Amount**
   - **Memo** (optional)
3. The total of the splits has to match the transaction's total.

> **Worked example:** Target run, $87.43 total. Of that, $54 was groceries and $33.43 was household stuff (cleaning supplies, light bulb, that thing for the cat). One transaction, two splits, two categories. savr shows the right amount in each category's spending.

You can have as many splits as you need. Remove a split by deleting its row — if only one remains, savr converts the transaction back to a normal (non-split) transaction.

---

## Debt payments

Debt payments are a specialized transaction type for paying down a loan account. They give you a clean breakdown of the three things a loan payment usually includes:

| Component | Where it goes |
|---|---|
| **Principal** | Reduces the loan account's balance |
| **Interest** | Posts as an expense in the linked payment category |
| **Fees** | Posts as an expense in the linked payment category |

To record a debt payment:

1. Open **New Transaction** and switch to **Debt Payment** mode.
2. Pick the **source account** (where the money comes from — usually checking).
3. Pick the **loan account** being paid down.
4. Enter the **principal**, **interest**, and **fees** amounts.
5. Confirm the payment category (defaults to the one linked to the loan).
6. Save.

Your checking balance drops by the total payment, the loan balance drops by the principal, and interest plus fees show up as spending in the payment category. No mental math required.

> **Worked example:** Your $1,247 mortgage payment is $983 principal + $251 interest + $13 fees. You record the payment as Debt Payment:
> - Checking: -$1,247
> - Mortgage loan balance: -$983
> - Mortgage Interest category Spent: +$264 (interest + fees)
> 
> Next month the principal goes up a bit and the interest goes down. savr captures this faithfully without you having to redo the math.

For payments that happen on a schedule, see [Recurring debt payments](../recurring/#recurring-debt-payments).

---

## Cleared status

Each transaction has a **cleared** flag. It's a simple way to mark transactions that have been confirmed by your bank — useful when you're matching your records against a statement.

Two common workflows:

- Reconcile against a statement once a month, marking each line cleared as you go. (savr's [Reconciliation](../reconcile/) flow does this automatically — recommended.)
- Leave recently entered transactions uncleared until they post on your bank's side.

The cleared flag is informational only — it doesn't change balance calculations.

---

## Edit and delete transactions

Click any transaction in the list to open its edit dialog. You can change any field, including converting a regular transaction into a split or back. Click **Save** to apply.

To remove a transaction, open the edit dialog and click **Delete**. Deletes are permanent and the affected account's balance updates immediately.

> **Heads up:** **Opening balance transactions** are special. They're auto-created with each account and don't affect budgets. You can edit the amount if you mistyped your starting balance, but you can't delete the opening balance entry without deleting the account itself.

---

## Filters

The Transactions page has a filter bar across the top so you can find activity quickly:

| Filter | What it does |
|---|---|
| **Account** | Show transactions for one specific account |
| **Category** | Show transactions in a specific category |
| **Payee** | Show transactions with a specific payee |
| **Type** | Restrict to Income, Expense, Transfer, or Credit |
| **Date range** | Pick a start and end date |

Filters combine with **AND** logic — every constraint applies. To clear, hit the reset button or remove filters one at a time.

> **For example:** Want to see everything you spent at "Whole Foods" this year? Filter by Payee = Whole Foods, Type = Expense, Date range = January 1 to today. There's your number.

---

## Pagination

Long transaction lists load in pages of 50. As you scroll near the bottom, savr fetches the next batch automatically. There's no "next page" button — just keep scrolling.

For very large queries, set a date range filter rather than scrolling through everything.

---

## Recurring transaction links

Transactions created from a [recurring rule](../recurring/) keep a reference to the rule that produced them. So you can trace any transaction back to its template, and savr can keep your recurring schedule accurate.

Edits to a transaction created by a recurring rule don't change the rule itself — only that one occurrence. (Want to change the rule? Edit it directly on the Recurring page.)

---

## Bulk import

Got a CSV from your bank? Don't type a year of transactions by hand.

The [Import & Export](../import-export/) page covers savr's three-step CSV import wizard, including how to map columns from any bank's export format and how to avoid duplicates against transactions you've already entered.

---

## Account detail view

Every account has a detail page that shows the same transaction list, scoped to just that account. Use it to:

- Reconcile against a paper or online statement (or click **Reconcile** for the guided flow)
- Quickly add a bunch of transactions for one account
- Review activity over a specific period without setting account filters

It's the same Transactions page you already know — just narrower.
