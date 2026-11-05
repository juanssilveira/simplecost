# simplecost

A Claude Code mod that shows a compact usage line under the prompt.

```
🧠 23% • 🕔 62% • $1.24
```

## What it shows

| Item | Meaning | Appears at | Yellow | Red |
|------|---------|------------|--------|-----|
| 🧠 | Context window used | 10% | 40% | 60% |
| 🕔 | 5-hour rate limit | always | 70% | 90% |
| 📅 | Weekly rate limit | 60% | 80% | 90% |
| 💳 | Gateway spend limit | always | — | — |
| `$` | Session cost | always | — | — |

Rate limits only appear on a Claude subscription or a gateway with a spend limit. Once yellow or red, they also show the time until they reset, like `🕔 85% (1h)`.

When the line doesn't fit the terminal, gray items drop out first, then yellow, then red.

## Install

In a Claude Code session, run:

```
/plugin install simplecost --marketplace juanssilveira/simplecost
```

Answer `y` to add the marketplace, then pick a scope.

## Usage

- `/toggle <item>` cycles an item through auto, hidden and always shown. Items: `ctx`, `5h`, `weekly`, `spend`, `cost`.
- `/toggle` lists every item with its current mode.

To change the thresholds, set the 🧠, 🕔 and 📅 rows in `/config`. Each takes three percentages: where the item appears, turns yellow and turns red, like `10 40 60`.

## Limitations

Mods are an early-access Claude Code feature, and the API may change between releases. Built and tested on Claude Code 2.1.312.
