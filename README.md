# SpendLog

Log what you spend, know what's left.

An offline‑first Flutter spend logger with runway math. Set a balance, a daily budget, and a target date, log what you spend, and it tells you when the money runs out at your current pace. No account, no server, everything stays on the phone.

## What It Does

- **Home tab**: Greeting, hero number “Left in the pot” with days‑to‑go, three stats (daily budget, today free, today spent), per‑category spend cards, calendar heat map, and a “Log a spend” input card.
- **Log tab**: List every expense grouped under Today / Yesterday / older dates. Filter chips narrow by category. Long‑press a row to delete with confirmation.
- **Settings tab**: Set your name, adjust balance / daily budget / target date, view categories, and edit individual category names, colors, icons, budgets, and keywords.

## Storage

Everything lives in SharedPreferences under `vector.*` keys (e.g., `vector.balance`, `vector.user_name`, `vector.expenses_json`). Keyed so the app never overwrites saved data with defaults on startup. Deleting the app deletes the data.

## Home‑Screen Widget

`RunwayWidget` (Android) shows days of runway and what is left free today without opening the app.

## Design

Cards are liquid glass: blurred backdrop, two‑stop white gradient, hairline border, soft shadow. Bottom bar is glass too — floating pill with accent‑gradient active states for Home / Log / Settings. Type follows Apple hierarchy with large titles; labels are conversational (“Left in the pot”, “Each day”, “Today free”).

## Build and Test

```bash
flutter pub get
flutter test
flutter build apk --release --split-per-abi
```

CI builds and tests on every push to `main`.

## Privacy

On‑device only. No account, no tracking, no network calls.

This app computes and reports; it is not investment advice.

## Licence

MIT — Joshua Riangkamang