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

