---
title: Recurring
parent: English
nav_order: 6
---

> 🌐 Lee esta página en [Español](../../es/recurring/)

# Recurring Transactions

Recurring transactions are templates that generate real transactions on a schedule. Use them for anything predictable: paychecks, rent, subscriptions, loan payments, regular savings transfers.

Each recurring rule keeps track of when it should next fire. When the next date arrives, savr can apply the rule and create an actual transaction in the underlying account.

---

## Frequencies

Five recurrence frequencies are available:

| Frequency | Description |
|---|---|
| **Daily** | Every day |
| **Weekly** | Every 7 days |
| **Biweekly** | Every 14 days — common for paychecks |
| **Monthly** | Same day each month |
| **Yearly** | Same day each year |

You can also set an optional **end date** to stop a recurrence (useful for finite obligations like an installment plan or a 12-month subscription).

---

## Create a recurring transaction

1. Open **Recurring** and click **New recurring**.
2. Choose a **type**:
   - Income — a regular paycheck or other income
   - Expense — a recurring bill, subscription, or fee
   - Transfer — automatic movement between two of your accounts (e.g. paycheck → savings)
   - Credit — recurring refund or rebate
   - Debt Payment — a loan payment with principal/interest/fees breakdown
3. Set the schedule:
   - **Frequency**
   - **Start date** — first occurrence
   - **End date** (optional) — stop after this date
4. Fill in the transaction details:
   - **Account** (and **to account** for Transfer)
   - **Amount**
   - **Category** (or splits — see below)
   - **Payee** (optional)
   - **Memo** (optional)
5. Save.

The recurring rule is saved with a **next date** equal to your start date. From then on, it advances each time the rule is applied.

---

## Splits in recurring transactions

Recurring rules support the same split functionality as one-off transactions. Toggle **Split** in the recurring editor and add rows for each category. The split totals must match the rule's amount.

When the rule is applied, the resulting transaction inherits the splits.

---

## Recurring debt payments

For loan payments, set the type to **Debt Payment** and provide:

- **Source account** — where the money comes from (typically checking)
- **Loan account** — the loan being paid down
- **Principal** — amount that reduces the loan balance
- **Interest** — amount posted as expense to the payment category
- **Fees** — amount posted as expense to the payment category

Each time the rule fires, savr creates a paired entry that drops the loan balance by the principal and posts interest and fees as spending in the linked category.

This is the cleanest way to track an amortizing loan: the principal portion grows automatically each month while interest typically shrinks, and you don't have to recalculate the breakdown manually.

---

## Applying due transactions

A recurring rule is **due** when its next date is today or in the past. Until the rule is applied, no actual transaction exists — only the template.

### Apply due

1. Open **Recurring**.
2. Due rules are listed at the top with an **Apply** action.
3. Click **Apply due** to fire all due rules at once, or apply them individually.

For each rule applied, savr:

- Creates a real transaction with the rule's details
- Stamps the transaction with a reference back to the recurring rule
- Advances the rule's next date by one period

### Why isn't it automatic?

Application is manual on purpose. It gives you a chance to review the entry before it lands in your account history — useful when an amount has changed (rent went up, subscription renewed at a higher price) or you want to skip a month.

If a rule is overdue by multiple periods (e.g. a weekly rule unrun for a month), applying it once creates one transaction and advances the next date by one period. Apply it repeatedly to catch up.

---

## Edit and delete

### Edit a rule

Click any recurring rule to edit it. You can change the frequency, dates, amount, splits, or any of the linked accounts and categories.

Editing the rule does **not** retroactively change transactions that were already created from earlier applications. To change a past transaction, edit it directly on the Transactions page.

### Delete a rule

Click **Delete** in the editor. Deleting a recurring rule does **not** delete the transactions that were created from it — your history stays intact. You're only removing the future schedule.

---

## Tips

- **Start with paychecks and rent.** These are predictable and high-impact — getting them automated frees you from copy-pasting them every month.
- **Set realistic next dates.** If your paycheck always lands on Fridays, pick the next Friday as the start date so the cadence is right.
- **Review before applying.** Use Apply Due as a checkpoint, not a fire-and-forget. Subscriptions creep up; rents change; reviewing each occurrence catches it early.
- **Use end dates for finite obligations.** A 12-month gym membership or 36-month auto loan can have an end date set, so the rule retires itself.
- **Pair with targets.** A recurring expense category with a Monthly target equal to the recurring amount is the savr equivalent of "set it and forget it."
