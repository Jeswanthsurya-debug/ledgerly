# ledgerly
# Ledgerly

**Ledgerly** is a lightweight, single file back office web app built for solo operators and independent educators (demonstrated with **Priya’s Home Tuitions**) to stay on top of receivables, upcoming bills, and short term cash flow without spreadsheet clutter.

It is designed around three everyday questions:
* **Who owes me?** Track open invoices, overdue aging, and how reliably each payer settles on time.
* **Will I have enough cash?** Project cash balances over 30, 60, or 90 days and test late payment scenarios before a crunch hits.
* **What should I do today?** Surface priority fee follow ups, cash low warnings, and upcoming bills in one place.

---

## Key Features

* **Overview Dashboard**
  * Displays cash in hand, total amount owed, overdue totals, and the lowest projected cash point over the next 30 days.
  * Breaks open invoices into aging buckets (**Not due**, **1–14 days**, and **15+ days**) alongside a payer reliability view based on average days late.
  * Highlights immediate actions under **Do this today** with quick buttons to draft reminders or mark invoices paid.

* **Fast One Line Invoicing**
  * Create invoices quickly from a single text input (for example, `zoya 3500 due 7`, or just a student/parent name to use their saved monthly fee with a default 7 day due date).
  * Marking an invoice **Paid ✓** adds the amount to cash in hand and updates payer lateness averages in Live mode.

* **Tone Aware WhatsApp Reminders**
  * Generates a reminder message tailored to how many days a payment is overdue (**Friendly**, **Polite but direct**, or **Firm**).
  * Opens a prefilled WhatsApp chat (`wa.me`), lets you copy the message with one click, and tracks how many times an invoice has been chased.

* **Cash Forecast & "What If" Simulator**
  * Plots projected cash balances across **30**, **60**, and **90 day** horizons with a `₹0` reference line and lowest balance marker.
  * Includes a **What if…** simulator where you can pick a parent and adjust a delay slider (0 to 45 days late) to see how late payments affect your lowest cash balance and date.

* **Ask Ledgerly Assistant**
  * Built in chat drawer with quick prompts (`Who owes me the most?`, `Will I run out of cash?`, `What if Ravi pays 20 days late?`, `Remind Joseph`).
  * Supports tool assisted responses via `claude.use('sample')` when available, with an automatic local fallback for common questions and actions.

* **Demo Mode, Guided Tour & Live Mode**
  * **Demo** loads sample tuition data (`Priya’s Home Tuitions`) and includes a **▶ Play tour** walkthrough.
  * **Live** starts from zero with a quick setup card to enter cash in hand, customers, and recurring bills.

---

## Getting Started

No build tools, package managers, or backend servers are required:

1. Clone or download the repository containing `Ledgerly — the one-person back office.html` (or rename it to `index.html`).
2. Open the HTML file directly in any modern web browser (desktop or mobile).
3. Switch between **Demo** and **Live** in the top bar as needed.

---

## Technical Notes

* **Single File Architecture:** Styles (including light and dark theme support) and application logic live inside a single HTML file using plain HTML, CSS, and vanilla JavaScript.
* **Session State:** Data is held in memory during the active session and resets when switching modes or reloading the page.
