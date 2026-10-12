# Bond math

`bondmath.py`, a small bond math module written in Python for Fixed Income, a free course series, with its tests.
Every expected value in `test_bondmath.py` is Excel's own result, stored in the two reference files beside it.

> This course is educational content created in a personal capacity. Nothing here is investment advice or a recommendation to buy or sell any security. All portfolio data is synthetic.

Run the tests with `python -m pytest -q test_bondmath.py`.

## Conventions

The units of every function in `bondmath.py`, as its docstring states them:

* `coupon_pct` and `yield_pct` are annual rates in percent: 7.0 means 7 percent.
* Prices and accrued interest are per 100 of face.
* Durations are in years, convexity in years squared, spreads in basis points.
* DV01 is in price points per 100 of face for one basis point, on the dirty price: modified duration x (clean price + accrued) x 0.0001, Excel's `=MDURATION(...)*(PRICE(...)+accrued)/10000`.
