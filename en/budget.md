> 🌐 Lee esta página en [Español](../es/budget.md)

# Budget

The Budget page is the heart of savr. Each month you decide how every unit of money is spent before it leaves your account.

---

## The To Be Budgeted banner

The **To Be Budgeted (TBB)** banner is fixed at the top of the page and always visible as you scroll through your categories. It shows:

- The amount of income still unassigned
- A rotating phrase that changes each time the scenario shifts

| Scenario | What it means |
|---|---|
| Positive amount | You have money waiting to be assigned to categories |
| Zero | Every unit is accounted for — fully budgeted |
| Negative (red) | You've assigned more than you have — reduce some categories |

The phrase uses your account's configured currency name (e.g. "Every US dollar has a job" or "Cada euro tiene un destino"), and there are 20 different phrases per scenario so the experience stays fresh.

---

## Reading the budget table

Categories are organized in collapsible groups. For each category you can see:

| Column | What it shows |
|---|---|
| Category | The category name (supports emoji and unicode) |
| Budgeted | How much you assigned this month |
| Spent | Actual spending recorded so far |
| Available | Budgeted + carry-over − spent |

### Progress bar

Each category row has a **progress bar** directly below the category name. It gives you an instant visual of how much of the available balance has been used:

- **Dark green** — unspent available balance
- **Light green** — spent portion (within budget)
- **Red / yellow** — overspent

A legend below the bar always shows the exact figures: how much was spent, how much remains, and whether there is carry-over from last month.

---

## Assigning money

Click any amount in the **Budgeted** column and type a new value.

- Press **Enter** to save
- Press **Escape** to cancel without making any changes
- Click away to save

---

## The category detail panel

Click any category **row** to open the detail panel on the right side of the screen. The panel stays fixed as you scroll, so it's always accessible.

### Stats breakdown

| Stat | What it shows |
|---|---|
| Carry-over | Unspent balance rolled in from the previous month |
| Assigned this month | The amount you budgeted for this month |
| Cash spending | Spending charged to non-credit accounts |
| Credit spending | Spending charged to credit card accounts |
| **Available** | The net balance (carry-over + assigned − spending) |

If the category is overspent, a warning shows how much is in the red.

### Auto-assign strategies

The panel offers five strategies to fill this category automatically:

| Strategy | What it does |
|---|---|
| **Underfunded** | Tops up to the target amount; never reduces what's already assigned |
| **Assigned last month** | Copies the amount you assigned in the previous month |
| **Spent last month** | Matches your actual spending from last month |
| **Zero Available** | Adjusts budgeted so the available balance becomes exactly zero (can release carry-over back to TBB) |
| **Zero Budgeted** | Removes all assigned money, setting budgeted to zero |

Each strategy card shows a preview delta (+/−) before you commit. If you don't have enough unassigned money (TBB), the amount is automatically capped and a warning is shown. Click **Apply** to confirm.

### Target

The panel shows the active target for the category along with its status (on track, underfunded, or unfunded). Click **Edit** to change the target, or **Set target** if none exists yet.

### Action buttons

| Button | When it appears | What it does |
|---|---|---|
| Cover overspending | Category is in the red | Opens the cover modal to pull funds from another category |
| Move money | Available balance is positive | Opens the move money modal |
| View transactions | Always | Filters the transaction list to this category for the current month |
| View history | Always | Shows all budget assignments made to this category this month |

---

## Quick-action buttons on rows

Two icon buttons appear on each category row when you hover:

- **⇄** — appears when the available balance is positive; opens the move money dialog
- **▼ (fill icon)** — appears when the category is overspent; opens the cover overspending dialog

These let you take action without opening the detail panel.

---

## Moving money

1. Click **⇄** on a category row, or open the detail panel and click **Move money**.
2. Select the destination category.
3. Enter the amount to transfer.

### Covering overspending

When a category goes negative, click the fill icon on the row or **Cover overspending** in the panel. Select a source category to pull funds from.

---

## Targets

A target tells savr how much a category should receive each period. Targets power auto-fill and show whether a category is on track at a glance.

### Setting a target

Open the category detail panel and click **Set target** or **Edit** next to the existing target badge. Choose a type:

| Type | Description |
|---|---|
| Monthly | A fixed amount each month |
| Weekly | Amount × weeks in the month |
| Yearly | Total divided evenly across 12 months |
| Custom | A specific total amount by a target date |

Enable **Rollover** if unspent money should carry forward (useful for irregular or annual expenses).

---

## Auto-Assign (all categories at once)

The **Auto-Assign** button at the top of the budget table fills all categories simultaneously. Choose a strategy and savr caps each category so you never exceed your TBB balance.

### Fill by Targets

The **↓ Fill by targets** button fills all categories that have a target set, in one step.

---

## Navigating months

Use the **← →** arrows at the top to move between months, or click **This month** to return to the current month. The TBB banner and month navigation stay fixed while only the category table scrolls.

Past months are read-only — you can review allocations and spending but cannot edit them.

---

## Hidden categories and groups

Hidden categories are invisible by default. Click **Show hidden** (appears in the navigation bar when hidden items exist) to reveal them temporarily. Manage visibility from the **Categories** page.
