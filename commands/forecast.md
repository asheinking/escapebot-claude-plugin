---
description: EscapeBot custom forecast and its drivers for a ticker
---

Look up the EscapeBot custom forecast for $ARGUMENTS.

1. Resolve the symbol with `search_symbols` if needed.
2. Call `get_prediction` for the forecast.
3. Call `get_oracle_decision_path` before explaining what drives it.
4. Do not invent forecasts. Do not place trades.
