# Simple Banking UI

A tiny front-end app to deposit and withdraw money and keep the balance in the browser.

Files:
- `index.html` — UI (balance display, input, buttons).
- `styles.css` — styling and responsive layout.
- `script.js` — balance state, validation, and event handlers.

Run:
1. Open `index.html` in a browser.
2. Enter an amount and click Deposit or Withdraw.

Quick behavior notes:
- Starts from `bankBalance` in `localStorage` or defaults to 1000.
- Amounts must be > 0; shows an error or "Insufficient funds!" when invalid.
- Balance updates immediately and is saved to `localStorage`.

Next ideas: add currency formatting or a transaction history.
# Simple Banking UI
A tiny front-end app to deposit and withdraw money and keep the balance in the browser.
Files:
- `index.html` — UI (balance display, input, buttons).
- `styles.css` — styling and responsive layout.
- `script.js` — balance state, validation, and event handlers.
Run:
1. Open `index.html` in a browser.
2. Enter an amount and click Deposit or Withdraw.
Quick behavior notes:
- Starts from `bankBalance` in `localStorage` or defaults to 1000.
- Amounts must be > 0; shows an error or "Insufficient funds!" when invalid.
- Balance updates immediately and is saved to `localStorage`.
Next ideas: add currency formatting or a transaction history.

# Simple Banking UI

This is a small front-end project that demonstrates a minimal banking interface built with HTML, CSS, and JavaScript. It lets a user deposit and withdraw money and keeps the balance in `localStorage` so it persists across page reloads.

## Files

- `index.html`: The HTML structure for the app — a balance display, an amount input, buttons for deposit and withdraw, and an error message area.
- `styles.css`: Styling for the UI (layout, colors, responsive tweaks, and simple form states).
- `script.js`: The JavaScript that manages balance state, input validation, and user interactions.

## How to run

1. Open `index.html` in a browser (double-click or use a local web server).
2. Use the input to enter an amount and click `Deposit` or `Withdraw`.
3. The balance updates immediately and is saved to the browser's `localStorage`.

## What the code does

- On load, the app checks `localStorage` for a saved balance (`bankBalance`). If none is found it starts with a default of 1000.
- The balance is shown inside the element with id `balance-display`.
- The input with id `amount` accepts a numeric value (allows decimal cents via `step="0.01"`).
- Clicking `Deposit` reads the number, validates it (must be > 0), then adds it to the balance, updates the display, and saves the new balance to `localStorage`.
- Clicking `Withdraw` also validates the number. If the value is greater than the available balance, an "Insufficient funds!" message appears. Otherwise it subtracts the amount and updates/saves the balance.
- The form's submit is prevented (the deposit button uses form submit behavior but JS prevents the default to keep everything client-side).
- While typing, the input is validated live: valid input hides the error and gives the input a green outline (via a `.valid` class); invalid input shows the error message.

## Key functions and lines to look at in `script.js`

- `updateBalance()` — updates the `balance-display` text and writes the balance to `localStorage`.
- `validateAmount(amount)` — returns `true` only for numeric amounts greater than zero.
- Event listeners:
	- `depositBtn.addEventListener('click', ...)` — handles deposits.
	- `withdrawBtn.addEventListener('click', ...)` — handles withdrawals and checks for insufficient funds.
	- `amountInput.addEventListener('input', ...)` — live validation and UI feedback.
	- `form.addEventListener('submit', ...)` — prevents the page from reloading on form submit.

## Styling notes

- CSS variables in `styles.css` manage colors, spacing, and font sizes for easy tuning.
- The layout centers the app and keeps it responsive for small screens.
- Input states use `.valid` and `:invalid` styles to provide visual feedback.

---

