---
description: EscapeBot fair value for a ticker
---

Look up EscapeBot fair value for $ARGUMENTS.

1. Resolve the symbol with `search_symbols` if needed.
2. Call `get_valuation` and report **fair_value**.
3. Use `get_valuation_growth` if the user asks how growth was served.
4. Do not invent a number. Do not place trades.
