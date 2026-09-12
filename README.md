# CashFlow101Clone

**CashFlow101Clone** is a fan-made browser clone of a classic personal-finance board game, rebuilt from scratch with additional game modes and rule customization that open up many unique ways to play. If you know the original board game, the rules will feel instantly familiar.

It is a pure static web game — no build tools, no backend. Just open `index.html` in a browser and play.

## What This Project Is

A from-scratch recreation of the classic board game's financial-education gameplay, designed to teach real-world skills through play:

* Practice real-world investing.
* Employ financial strategies.
* Leverage assets and liabilities.
* Manage income, expenses, and passive income to escape the Rat Race.

### Game Modes
* **Fast Track Mode** — After escaping the Rat Race, players start with a big bank account and play toward their dreams in the Fast Track
* **Hard Mode** — Extra doodads, limited loans
* **Same Career Mode** — Every player starts with the same career, savings, and debts

### Rule Customization
* **Insurance** — Avoid downsizing by paying an insurance fee each paycheck
* **Big Families** — Raise the limit of children players can have
* **Liquidating Assets** — Sell assets for 50% back to the bank when threatened by bankruptcy
* **Doodads with Paychecks** — More doodads; players who land on a paycheck space also draw a doodad card
* **Mortgage Payments** — Adds realistic mortgage payments
* **Job Choice** — Option to choose jobs
* **Speed Start** — Players start with their total income in their savings

## Credits & Thanks

Almost all of this game's engine and content was originally created by **Samuel Wright** — see the original project at [sleighs/CashFlowJs](https://github.com/sleighs/CashFlowJs).

This repository is a fork of that work, built on top of it. I'm deeply grateful to Samuel for open-sourcing the original under the MIT License, which made this secondary development possible.

## Changes Made in This Fork

Based on the original `CashFlowJs`, this fork focuses on fixing the game's financial calculation bugs.

* **Fixed the Fast Track PAYDAY bug (High)**
  * Previously, payday in the Fast Track was calculated as *passive income × 2* (passive income was double-counted), paying out far too much money each Cash Flow Day and breaking game balance. It now correctly uses the Cash Flow Day income.
* **Fixed Fast Track total income double-counting**
  * Acquiring a Fast Track asset added its cash flow to the total income twice. It is now counted once.
* **Fixed the Fast Track starting base**
  * The starting Cash Flow Day income now uses passive income × 100, as per the official rules, instead of an incorrect base.
* **Fixed win-condition consistency**
  * The progress bar and the victory check now use the same metric, so what players see matches how the game decides the winner.
* **Fixed paycheck settlement across payday spaces**
  * Fixed a bug where crossing a payday square did not always settle the paycheck correctly, ensuring every payday line that a player passes grants the proper payment.

## Play It

The game is fully static. Open `index.html` directly in any modern browser.

## License

This project is released under the **MIT License**.

```
Copyright (c) 2019 Samuel Wright
Copyright (c) 2026 Dr-Asimov
```

See the [LICENSE](LICENSE) file for the full text.

---

This is a fan creation made for educational and personal amusement. This game is not sold or distributed. I do not own or have rights to the *CashFlow* trademark.