> 🌐 Lee esta página en [Español](../es/getting-started.md)

# Getting Started with savr

savr is a zero-based budgeting app — every unit of your income is assigned a job before you spend it. When your budget is balanced, the **To Be Budgeted** amount reaches zero and you know exactly where your money is going.

## How savr works

1. **Add your accounts** — checking, savings, credit cards, loans, cash.
2. **Create categories** — group similar expenses (Housing, Food, Transport, etc.).
3. **Budget your income** — assign all available money to categories until nothing is left unassigned.
4. **Record transactions** — every purchase reduces the available balance in the matching category.
5. **Adjust as you go** — if you overspend in one category, move money from another.

---

## Quick setup (first time)

### 1. Create your accounts

Go to **Accounts** and add each account you want to track. Enter the current balance as of today — this becomes your starting point.

For credit cards, enter the current balance owed as a positive number (e.g. `450.00`). For loans, you'll also enter the interest rate and monthly payment.

### 2. Set up categories

Go to **Categories** and organize your spending into groups and categories. You can use emojis and unicode characters in category names to make them easier to scan at a glance. For example:

```
🏠 Housing
  ├─ Rent
  └─ Utilities

🍔 Food
  ├─ Groceries
  └─ Restaurants

🚗 Transport
  ├─ Fuel
  └─ Insurance
```

You can drag categories and groups to reorder them at any time.

### 3. Budget this month

Go to **Budget**. The **To Be Budgeted** banner shows your total unallocated money. Click the **Budgeted** amount next to any category and type in how much you want to assign. Press **Enter** to save or **Escape** to cancel. Keep going until the banner reads **0.00** and shows a congratulatory message.

If you have budget targets set, use **Auto-Assign** or **Fill by targets** to fill categories automatically.

### 4. Record your spending

Every time you spend money, add a transaction in the **Transactions** page or directly inside an account. Select the right category and the available balance updates instantly.

---

## Key concepts

### To Be Budgeted (TBB)

The amount of income you haven't assigned to any category yet. This number should reach **zero** — not go negative. If it's negative, you've budgeted more than you have and need to reduce some categories.

The TBB banner displays a rotating motivational phrase that changes each time you move between scenarios (money to assign, fully budgeted, or over-budgeted). The phrase uses your account's currency name automatically.

### Available balance

Each category shows an **Available** amount: what you budgeted plus any carry-over from last month, minus what you've spent. A **progress bar** below the category name shows the spending ratio at a glance. If the available balance turns red, you've overspent and need to cover it by moving money from another category.

### The category detail panel

Click any category row to open a detail panel on the right side. It shows a breakdown of carry-over, assigned money, cash spending, credit spending, and the net available balance. It also lets you apply per-category auto-assign strategies and manage the category's target — all without leaving the budget page.

### Targets

A target is a goal for a category — how much you want to budget each month, week, or year. Targets drive the **Auto-Assign** and **Fill by targets** features.

### Rollover

When a category has money left at the end of the month and rollover is enabled, that surplus carries forward into the next month's available balance.
