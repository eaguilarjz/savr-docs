---
title: Recurring
parent: English
nav_order: 6
---

> 🌐 Lee esta página en [Español](../../es/recurring/)

# Recurring Transactions

Most of your financial life is repeats. Rent on the 1st. Spotify on the 12th. Paycheck every other Friday. Recurring transactions are templates that fire on a schedule, so you don't retype the same things 50 times a year.

Each recurring rule keeps track of when it should next fire. When that day comes, savr is ready to apply the rule and create a real transaction in the underlying account.

---

## Frequencies

Five recurrence options:

| Frequency | Description |
|---|---|
| **Daily** | Every day |
| **Weekly** | Every 7 days |
| **Biweekly** | Every 14 days — the classic paycheck cadence |
| **Monthly** | Same day each month |
| **Yearly** | Same day each year |

You can also set an optional **end date** to stop a recurrence (useful for finite obligations like a 12-month installment plan or a yearlong subscription).

---

## Create a recurring transaction

1. Open **Recurring** and click **New recurring**.
2. Choose a **type**:
   - **Income** — paycheck, recurring royalty, regular Venmo from your roommate
   - **Expense** — recurring bill, subscription, gym membership
   - **Transfer** — automatic movement between two of your accounts (e.g. paycheck → savings)
   - **Credit** — recurring refund or rebate
   - **Debt Payment** — loan payment with principal/interest/fees breakdown
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

The rule is saved with a **next date** equal to your start date. From then on, it advances each time the rule fires.

> **Worked example — your paycheck:** You get paid biweekly on Fridays, $2,400 net. Set up:
> - Type: Income
> - Frequency: Biweekly
> - Start date: this Friday
> - Account: Checking
> - Amount: $2,400
> - Payee: Acme Corp Payroll
> 
> From now on, every other Friday, you'll see "Apply" next to this rule. One click and the income lands in your account, ready to be budgeted.

---

## Splits in recurring transactions

Recurring rules support splits, just like one-off transactions. Toggle **Split** in the editor and add a row for each category. The split totals have to match the rule's amount.

When the rule fires, the resulting transaction inherits the splits.

> **For example:** Your paycheck has $1,800 take-home and $600 going to a savings sub-account. You set up the income rule with two splits — $1,800 to "Paycheck → Checking" and $600 to "Paycheck → Savings." Each pay period, both land in their right places.

---

## Recurring debt payments

For loan payments, set the type to **Debt Payment** and provide:

- **Source account** — where the money comes from (typically Checking)
- **Loan account** — the loan being paid down
- **Principal** — amount that reduces the loan balance
- **Interest** — amount posted as expense in the payment category
- **Fees** — amount posted as expense in the payment category

Each time the rule fires, savr creates a paired entry that drops the loan balance by the principal and posts interest + fees as spending in the linked category.

This is the cleanest way to track an amortizing loan. The principal portion grows automatically each month, the interest typically shrinks, and you don't have to recalculate the breakdown manually. Set it once, apply each month, watch the loan balance trend toward zero.

> **Worked example — your mortgage:** Your $1,247 mortgage payment is roughly $983 principal + $251 interest + $13 escrow fees. Set up a Monthly Debt Payment rule with those numbers. Apply it each month. Over a year, you can update the principal/interest split a couple of times to match what your lender's amortization schedule is showing. Watch the mortgage account's balance shrink and feel something close to joy.

---

## Applying due transactions

A rule is **due** when its next date is today or in the past. Until you apply it, no actual transaction exists — only the template.

### Apply due

1. Open **Recurring**.
2. Due rules show up at the top with an **Apply** action.
3. Click **Apply due** to fire all due rules at once, or apply them individually.

For each rule applied, savr:

- Creates a real transaction with the rule's details
- Stamps the transaction with a reference back to the recurring rule
- Advances the rule's next date by one period

### Why isn't it automatic?

Application is manual on purpose. It gives you a chance to review the entry before it lands in your account history. This matters because:

- Subscriptions creep up in price ("Spotify just bumped me from $10 to $12")
- Rents change
- A "monthly" gym charge sometimes skips a month
- You want to see the recurring transaction *before* it affects your balance, not after

If a rule is overdue by multiple periods (a weekly rule unrun for a month), applying it once creates one transaction and advances the next date by one period. Apply it repeatedly to catch up — you'll get the right number of transactions for the right number of periods.

> **Pro tip:** Make checking the Recurring page a weekly ritual. Two minutes on Sunday night to apply whatever's due. Your transactions stay current, your bank reconciliations get easier, and you catch price increases the day they happen.

---

## Edit and delete

### Edit a rule

Click any recurring rule to edit it. You can change the frequency, dates, amount, splits, or any of the linked accounts and categories.

Editing the rule does **not** retroactively change transactions that were already created from earlier applications. To change a past transaction, edit it directly on the Transactions page.

### Delete a rule

Click **Delete** in the editor. Deleting a recurring rule does **not** delete the transactions that were created from it — your history stays intact. You're only removing the future schedule.

> **Common scenario:** You cancel that streaming service. Edit the recurring rule's end date to today, or just delete the rule. The 14 monthly transactions you've already recorded for it stay in your history. The future stops.

---

## Tips

- **Start with paychecks and rent.** These are predictable and high-impact. Getting them automated frees up two to five minutes per month and makes the rest feel easier.
- **Set realistic next dates.** If your paycheck always lands on Fridays, pick the next Friday as the start date so the cadence is right from day one.
- **Review before applying.** Use Apply Due as a checkpoint, not a fire-and-forget. The two-second review catches the price hikes that everyone else doesn't notice for six months.
- **Use end dates for finite obligations.** A 12-month gym membership, a 36-month auto loan — set the end date and the rule retires itself when it should.
- **Pair with targets.** A recurring expense category with a Monthly target equal to the recurring amount is the savr equivalent of "set it and forget it."
- **It's okay to skip.** If a recurring rule is due but you actually didn't get charged this month (the gym was closed for renovations, your roommate forgot to send the rent transfer), don't apply it. Bump the next date forward manually instead.
