---
title: Categories
parent: English
nav_order: 5
---

> 🌐 Lee esta página en [Español](../../es/categories/)

# Categories

Categories let you group your spending into meaningful buckets so the budget page stays organized and easy to read.

Every Expense and Credit transaction is assigned to a category, and every category lives inside a category group. The grouping is purely organizational — it has no effect on calculations.

---

## Why categories matter

Categories are the unit at which you allocate money on the Budget page and the unit at which spending is summed. Picking the right level of granularity is a balance:

- **Too few categories** → you can't see where money is actually going.
- **Too many** → the budget becomes tedious to maintain and you stop using it.

A common starting point: one category per recurring bill (rent, utilities, phone), one for each major variable expense (groceries, transportation, dining), and a few for goals and quality of life.

You can rename, reorder, hide, or delete categories at any time, so don't worry about getting the structure perfect upfront.

---

## Category groups

Groups are how categories are organized visually. Examples:

- **Bills** — Rent, Utilities, Phone, Internet
- **Variable** — Groceries, Transportation, Dining Out
- **Goals** — Emergency Fund, Vacation, New Car
- **Quality of Life** — Entertainment, Subscriptions, Hobbies

### Create a group

1. Open **Categories**.
2. Click **New group**.
3. Enter a name and save.

### Edit a group

Click the group name to rename it. You can also hide a group from the **edit** menu — see [Hiding](#hiding-categories-and-groups) below.

### Reorder groups

Drag a group's header up or down to change its position. The order applies everywhere groups are displayed (Budget, Categories, transaction selectors).

### Delete a group

To delete a group, every category inside it must first be deleted or moved to another group. savr will warn you if a group still contains categories.

---

## Categories

### Create a category

1. Open **Categories**.
2. Pick the group where the category belongs.
3. Click **New category** in that group.
4. Type the name and save.

> Category names support emoji. A leading 🛒 or 🏠 is a quick way to scan a long list.

### Edit a category

Click any category name to rename it inline. Press Enter to save, Escape to cancel.

To move a category to a different group, drag it across to the destination group's section.

### Reorder categories

Drag categories within a group to change their order. Order persists across sessions and is reflected on the Budget page.

### Delete a category

If the category has no transactions, you can delete it directly.

If the category **has transactions**, savr opens a **reassign** modal:

1. Pick another category to receive all the existing transactions.
2. Confirm.

savr moves every transaction to the new category and then deletes the old one. This keeps your history intact — no spending data is lost.

---

## Hiding categories and groups

Sometimes a category isn't relevant anymore (a one-time goal you finished, a service you canceled), but you want to keep its history. Instead of deleting:

1. Open the category's actions and toggle **Hide**.

Hidden categories don't appear on the Budget page, in transaction selectors, or in auto-assign strategies. The data is preserved, and you can unhide them at any time. The same applies to entire groups.

This is the cleanest way to retire a category that's served its purpose.

---

## How spending and budgeting interact

A few things to know about how categories behave:

- **Spending** in a category is the sum of Expense transactions less any Credit (refund) transactions for the selected month.
- **Budgeted** is the amount you've allocated this month — independent of spending.
- **Available** = Budgeted − Spent. When negative, the category is overspent.
- **Targets** can be set on any category to indicate what you want to budget. Targets drive auto-assign and the Fill by Targets shortcut. See [Budget → Targets](../budget/#targets-goals).

Hidden categories don't appear in the budget, but they still receive the transactions you've already assigned to them. To stop posting new transactions to a category, simply don't pick it when creating new ones — or delete it (with reassignment).

---

## Tips

- **Start with broad categories.** Add detail later if you find yourself wanting to track something specific.
- **Use groups for hierarchy, not categories.** It's tempting to make sub-categories like "Dining Out → Lunch" and "Dining Out → Dinner" — but a single "Dining Out" category with notes on each transaction is usually enough.
- **One category per real-world budget commitment.** If you have a fixed monthly bill, give it its own category so a target can track it cleanly.
- **Hide instead of delete** if you're unsure. Hiding is reversible; deletion (with reassignment) merges history into another category permanently.
