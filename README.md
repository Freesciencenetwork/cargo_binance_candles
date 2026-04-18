# binance_spot_candles

Small Rust library for **read-only** Binance Spot market data:

- `GET /api/v3/klines` → normalized `Candle` rows
- `GET /api/v3/exchangeInfo` → `SymbolFilters` (`tick_size`, `lot_step`)
- optional CSV kline parsing (Binance export format)

Published on **[crates.io](https://crates.io/crates/binance_spot_candles)** · API docs on **[docs.rs](https://docs.rs/binance_spot_candles)**.

## For users (installed tool)

Install the **`binance-fetch`** binary once:

```bash
cargo install binance_spot_candles
```

Then:

```bash
binance-fetch klines --symbol BTCUSDT --interval 15m --limit 100
binance-fetch symbol-filters --symbol BTCUSDT
```

## For Rust projects (library)

In `Cargo.toml`:

```toml
binance_spot_candles = "0.1.0"
```

## For maintainers (this checkout)

```bash
cargo run --bin binance-fetch -- klines --symbol BTCUSDT --interval 15m --limit 5
cargo publish
```
