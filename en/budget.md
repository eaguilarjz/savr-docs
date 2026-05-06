---
title: Budget
parent: English
nav_order: 2
---

> 🌐 Lee esta página en [Español](../../es/budget/)

# Budget

The Budget page is the heart of savr. Each month you decide how every unit of money is spent before it leaves your account. When the **To Be Budgeted** value reaches zero, every dollar has a job.

---

## Anatomy of the budget page

| Element | What it shows |
|---|---|
| **Month / year selector** | Navigate to any past or future month. The current month is selected by default. |
| **To Be Budgeted (TBB)** | Income you've received but haven't assigned to a category yet. The goal is to keep this at zero. |
| **Account balance total** | Sum of all your active account balances, displayed alongside the budget for context. |
| **Category groups** | Collapsible groupings of categories (e.g. "Bills", "Goals"). Each group shows aggregated metrics. |
| **Category rows** | Each category shows Budgeted, Spent, and Available for the selected month. |

Each category row has three core values:

- **Budgeted** — what you've allocated this month
- **Spent** — total transactions in this category this month
- **Available** — `Budgeted − Spent`. What you can still spend.

When **Available** is negative, the value turns red. That's a signal to move money in.

---

## Assigning money to categories

Click any category and enter the amount you want to budget for the month. Each assignment reduces **To Be Budgeted** by the same amount.

The objective for the month is simple:

> **Income − Allocations = 0**

If you have a balance left in TBB, you haven't planned for everything. If TBB goes negative, you've over-allocated and need to reduce somewhere.

### Income classification

How transactions affect TBB depends on their type:

| Transaction type | Effect on TBB |
|---|---|
| **Income** | Increases TBB |
| **Expense** | No direct effect (reduces category Available via Spent) |
| **Credit** (refund) | No effect on TBB. Reduces category Spent only. |
| **Transfer** | No effect — money moves between your accounts |

This means a refund correctly cancels out a previous purchase in your category, without inflating your income for the month.

---

## Moving money between categories

When one category is overspent and another has a surplus, you don't need to break the budget — you just move money.

1. Click the source category in the budget list.
2. Use the **Move money** action and pick the destination category and amount.
3. The transfer is recorded in the budget history of both categories.

Your overall **To Be Budgeted** stays at zero. Only the internal allocation changes.

---

## Auto-assign strategies

savr can fill out your budget automatically. Open the **Auto-Assign** menu on the Budget page and choose a strategy:

| Strategy | What it does | When it's useful |
|---|---|---|
| **Underfunded** | Fills each category up to its target (or up to what's already spent if no target). | Most common — gets every category to "covered" |
| **Assigned Last Month** | Copies the previous month's allocations. | Predictable months where nothing has changed. |
| **Spent Last Month** | Allocates each category what was actually spent last month. | Sanity-check budget against real spending. |
| **Zero Available** | Adds money to categories where Available is negative, bringing them back to zero. | Quick fix for overspending late in the month. |
| **Zero Budgeted** | Allocates to categories that have no budget yet this month. | Onboarding a new month from scratch. |

You can preview the total each strategy will assign before applying, and optionally cap the maximum amount to spend.

### Fill by Targets

The **Fill by Targets** button is a one-click shortcut: it fills every category that has a target with that target's suggested amount for the current month. Categories without a target are left untouched.

### Single-category auto-assign

You can also auto-assign a single category from its action menu. savr uses the category's target — or its previous spending — to suggest an amount.

---

## Targets (goals)

A target tells savr how much you want to budget for a category, so it can give you an at-a-glance status (on track, underfunded, unfunded) and power features like Fill by Targets.

### Target types

| Type | Behavior |
|---|---|
| **Monthly** | Recurring each month. Optionally tied to a specific day-of-month. |
| **Weekly** | Recurs each week on a chosen day (Sunday through Saturday). |
| **Yearly** | Recurs annually on a specific month and day. |
| **Custom** | Save a total amount by a target date. Can repeat every N months / years, or be one-time. |

### Setting a target

1. Click a category to open its detail panel.
2. Click **Set target**.
3. Choose the target type and amount.
4. For Custom targets, set the target date and (optionally) a repeat interval.
5. For Monthly targets, optionally enable **Rollover** so unspent budget carries over to next month.

### Status

Each category with a target shows one of three statuses:

- **OK** — Budget meets or exceeds target
- **Underfunded** — Budget is less than the target
- **Unfunded** — Nothing budgeted yet this month

### Removing a target

Open the category's target modal and click **Remove target**. The category remains; only the goal is cleared.

---

## Category detail panel

Click any category to open its detail panel. You'll see:

- **Budget history** — every allocation and money transfer for this category, oldest to newest
- **Cash vs. credit breakdown** — spending split between cash-style accounts (checking, savings, cash) and credit cards. Useful when reconciling a category against actual cash flow.
- **Recent transactions** — quick view of the activity driving the Spent value
- **Target status** — if a target is set

### Budget history entries

Two kinds of entries appear in the history:

| Entry type | What it represents |
|---|---|
| **Allocation** | Money you assigned directly to this category. |
| **Transfer** | Money moved in from or out to another category. |

---

## Tips for a healthy budget

- **Aim for TBB = 0.** Anything in TBB is unplanned money. Assign it.
- **Don't budget money you don't have.** Only what's already in your accounts can be allocated. Future income gets budgeted next month.
- **Adjust mid-month.** Overspending isn't failure — it's information. Move money from a flexible category (e.g. Entertainment) to cover it.
- **Use targets sparingly at first.** Get comfortable with manual assignment before relying on auto-fill.
- **Review at month-end.** A quick look at categories with a positive Available helps you decide whether to roll the surplus forward or reallocate it.
