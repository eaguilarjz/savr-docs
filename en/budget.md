---
title: Budget
parent: English
nav_order: 2
---

> {% include lang-globe.html %} Lee esta página en [Español](../../es/budget/)

# Budget

The Budget page is the heart of savr. It's where you make decisions instead of reacting to them.

Every month, you take what you have and tell each dollar what it's going to do. Rent. Groceries. Savings. The dentist appointment you've been putting off. By the time you're done, every dollar has a job, and you know — with actual numbers, not vibes — what's available for what.

It sounds boring written out like that. In practice it's surprisingly satisfying. Like organizing a closet, but for your money.

---

## Anatomy of the budget page

| Element | What it shows |
|---|---|
| **Month / year selector** | Move backward or forward through any month, past or future. The current month is selected by default. |
| **Ready to Assign** | The headline number at the top. This is income you've received but haven't given a job to yet. |
| **Account balance total** | Sum of all your active accounts, shown alongside the budget for context. |
| **Category groups** | Collapsible groupings of categories. Each group shows aggregated metrics. |
| **Category rows** | Each category shows Assigned, Spent, and Available for the selected month. |
| **Toolbar** | Holds the **Auto-Assign** menu, **Recent Moves**, and **Expand all / Collapse all** for the category groups. |

Each category row has three numbers:

- **Assigned** — what you've allocated this month
- **Spent** — what you've actually spent in this category this month
- **Available** — `Assigned − Spent`. The number you care about.

When **Available** goes negative, the value turns red. That's not a scolding — it's a signal that you should move money in from somewhere else.

> **Pro tip — inline adds.** Hover over any category-group row and a **+** button appears so you can add a category to that group without leaving the budget page. There's a matching **+ New group** affordance to add a whole new group inline. Same on mobile, just always visible.

---

## Assigning money to categories

Click a category. Type how much you want to spend there this month. Save. Repeat.

Each assignment reduces **Ready to Assign** by the same amount. The math you're doing is dead simple:

> **Income − Allocations = 0**

When the right side hits zero, every dollar has a job and you're done.

### Worked example

You start the month with $3,200 in your checking account, all earned this month. Ready to Assign shows $3,200.

You start clicking through categories:

| Category | Assigned | Ready to Assign after |
|---|---|---|
| Rent | $1,400 | $1,800 |
| Groceries | $500 | $1,300 |
| Utilities | $150 | $1,150 |
| Phone & Internet | $120 | $1,030 |
| Gas | $180 | $850 |
| Dining Out | $200 | $650 |
| Subscriptions | $40 | $610 |
| Emergency Fund | $300 | $310 |
| Vacation Savings | $200 | $110 |
| Hobbies | $110 | $0 |

Ready to Assign: $0. May is fully planned. You can spend with confidence because every dollar already knows what it's for.

### How transaction types affect Ready to Assign

How transactions affect Ready to Assign depends on their type:

| Transaction type | Effect on Ready to Assign |
|---|---|
| **Income** | Increases Ready to Assign |
| **Expense** | No direct effect (reduces Available in the category via Spent) |
| **Credit** (refund) | No effect on Ready to Assign. Reduces category Spent only. |
| **Transfer** | No effect — money moves between your accounts |

> **Why Credit doesn't add to Ready to Assign:** A refund cancels out a previous expense. If you bought $80 of groceries and returned $20 worth, your category should reflect $60 of net spending — not $80 spent + $20 of new income. That's exactly what Credit does. Use Income for actual new money: paychecks, gifts, interest earned.

---

## Moving money between categories

Here's the key insight that makes budgeting bearable: **you don't have to be perfect**.

You'll overspend somewhere every month. Restaurants is a classic — you have a couple of nights out, the category goes red. That's not a moral failing. It's information. The fix is one click:

1. Click the source category (the one with surplus).
2. Use the **Move money** action.
3. Pick the destination category and the amount.
4. Save.

Both categories now show the transfer in their history. Your overall Ready to Assign stays at zero. Nothing's broken — you just adjusted the plan.

> **Common scenario:** You budgeted $200 for Dining Out and ended up at $245. Available is -$45. You move $45 from Hobbies (where you've barely spent anything) into Dining Out. Both categories rebalance. Total budget unchanged.

This is the move that keeps people from ditching their budget mid-month. Embrace it.

### Recent Moves

Open **Recent Moves** from the Budget toolbar to see a chronological log of every assignment and money transfer for the current month. Entries are grouped by date (Today / Yesterday / Older), with three filter pills at the top:

- **All** — every change.
- **Moved** — only the transfers between categories.
- **Assigned** — only the direct allocations.

Useful when you can't remember which category you pulled $50 out of last week, or when you're reconciling end-of-month and want to see the order things happened in.

---

## Auto-assign strategies

savr can fill out your budget for you. Open the **Auto-Assign** menu on the Budget page and pick one of six strategies:

| Strategy | What it does | When to reach for it |
|---|---|---|
| **Underfunded** | Fills each category up to its target (or up to its uncovered shortfall — what you spent minus what carried forward — if no target). | Most common — gets every category to "covered" without double-funding things that already have a buffer. |
| **Assigned Last Month** | Copies last month's allocations as-is. | Predictable months where nothing changed. |
| **Spent Last Month** | Allocates each category what was actually spent last month. | A reality-check budget against your real habits. |
| **Zero Available** | Adds money to categories where Available is negative, bringing them back to zero. | Quick cleanup at the end of the month when a few categories are red. |
| **Zero Assigned** | Allocates to categories that have no budget yet this month. | Starting a new month from scratch. |
| **Reduce Overfunding** | Trims categories that have *more* assigned than they need — leaves each one at its target or its actual spending, whichever is higher. The opposite of Underfunded. | Pulling money back to **Ready to Assign** so you can redirect it elsewhere. |

You can preview the total each strategy will assign (or pull back) before applying, and optionally cap the maximum spend.

### Fill by Targets

The **Fill by Targets** button is a one-click shortcut: it funds every category that has a target with that target's suggested amount. Categories without a target are left alone.

This is most people's "set it and forget it" workflow once they've been at it a few months. Set targets on your real categories, click Fill by Targets at the start of each month, adjust the leftovers manually.

### Single-category auto-assign

Each category also has its own auto-assign action — useful when you just want to fill in one spot. savr suggests an amount based on the target (or your previous spending if there's no target).

---

## Targets (a.k.a. goals)

A target tells savr "this is how much I want to budget for this category." Once a target is set, savr can:

- Show you a status (on track, underfunded, unfunded) at a glance
- Power Fill by Targets for one-click monthly funding
- Suggest amounts in auto-assign

### Target types

| Type | Behavior |
|---|---|
| **Monthly** | Recurs every month. Optionally tied to a specific day-of-month. |
| **Weekly** | Recurs each week on a specific day (Sunday through Saturday). |
| **Yearly** | Recurs annually on a specific month + day. |
| **Custom** | Save a total amount by a target date. Can repeat every N months / years, or be one-time. |

> **For example:**
> - Rent — Monthly target of $1,400, due on the 1st.
> - Groceries — Weekly target of $125 (savr knows that's ~$540/month).
> - Car insurance — Yearly target of $720, due in October.
> - Vacation — Custom target of $2,400 by next August. savr suggests ~$200/month.

### Setting a target

1. Click a category to open its detail panel.
2. Click **Set target**.
3. Choose the target type and amount.
4. For Custom targets, set the target date and (optionally) a repeat interval.
5. For Monthly targets, optionally enable **Rollover** so unspent budget carries over to next month.

### Target status

Each category with a target shows one of three states:

- **OK** — assigned at or above the target
- **Underfunded** — budgeted but not enough
- **Unfunded** — nothing budgeted this month

### Removing a target

Open the category's target modal and click **Remove target**. The category sticks around; only the goal is cleared.

> **Pro tip:** Don't set targets on every category right away. Start with the boring fixed bills (rent, utilities, subscriptions). Add targets to variable categories only after you've watched your real spending for a couple months and have realistic numbers.

---

## The category detail panel

Click any category to open its detail panel. You'll see:

- **Budget history** — every allocation and money transfer for this category, oldest to newest. The audit trail of how this category got to where it is today.
- **Cash vs. credit breakdown** — spending split between cash-style accounts (checking, savings, cash) and credit cards. Useful when you want to know "okay, but how much of this is going to actually leave my checking account this month?"
- **Recent transactions** — quick view of what's been driving the Spent value
- **Target status** — if a target is set

### Budget history entries

Two kinds of entries appear in the history:

| Entry type | What it represents |
|---|---|
| **Allocation** | Money you assigned directly to this category. |
| **Transfer** | Money moved in from or out to another category. |

---

## Tips from people who actually do this

- **Aim for Ready to Assign = 0.** Anything in Ready to Assign is unplanned. Plan it. Even "Future Stuff" is a category you can park money in.
- **Don't budget money you don't have.** Only what's already in your accounts can be allocated. Future income gets budgeted next month, when it actually arrives.
- **Adjust mid-month without guilt.** Overspending isn't failure. It's data. Move money, keep going.
- **Use targets sparingly at first.** Get used to manual assignment for a month or two. You'll set better targets once you know your real numbers.
- **Review at month-end.** Spend two minutes looking at categories with surplus. Roll it into next month, throw it at savings, or move it to wherever you're behind. The leftover money is a gift to your future self — don't waste it.
- **Boring categories deserve love too.** A monthly target on rent feels pointless because you always pay it. But it makes Fill by Targets work without you having to think. Worth it.
