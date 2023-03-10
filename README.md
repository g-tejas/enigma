<!-- markdownlint-configure-file {
  "MD013": {
    "code_blocks": false,
    "tables": false
  },
  "MD033": false,
  "MD041": false
} -->

<div align="center">
<a href="https://github.com/othneildrew/Best-README-Template">
    <img height="100" src="https://images-wixmp-ed30a86b8c4ca887773594c2.wixmp.com/f/84a49b59-fcd9-4cc1-9896-10c237af55d0/dcb3lek-c2143f37-7e5f-45be-8291-51c4e69997cf.gif?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJ1cm46YXBwOjdlMGQxODg5ODIyNjQzNzNhNWYwZDQxNWVhMGQyNmUwIiwiaXNzIjoidXJuOmFwcDo3ZTBkMTg4OTgyMjY0MzczYTVmMGQ0MTVlYTBkMjZlMCIsIm9iaiI6W1t7InBhdGgiOiJcL2ZcLzg0YTQ5YjU5LWZjZDktNGNjMS05ODk2LTEwYzIzN2FmNTVkMFwvZGNiM2xlay1jMjE0M2YzNy03ZTVmLTQ1YmUtODI5MS01MWM0ZTY5OTk3Y2YuZ2lmIn1dXSwiYXVkIjpbInVybjpzZXJ2aWNlOmZpbGUuZG93bmxvYWQiXX0.mir1KAo6CAqMWYFAQ5SeZxw5138vRURUGegbbrYvc4A">
</a>
  <h2>enigma machine</h2>
<p align="center"><i>
    A high performance, multi-threaded, lock-free HFT systems monitoring GUI - batteries included!
    </i><br />
    <br />
    <a href="https://github.com/othneildrew/Best-README-Template">View Demo</a>
    ·
    <a href="https://github.com/othneildrew/Best-README-Template/issues">Report Bug</a>
    ·
    <a href="https://github.com/othneildrew/Best-README-Template/issues">Request Feature</a>
  </p>
  
  <figure>
    <img src="https://media1.tenor.com/images/589e7ed35c66cfda5a4d2ecf4c9559d0/tenor.gif?itemid=27442143">
    <br>
    <figcaption><em>GIF is rendered at 10fps, can't upload larger size for some reason, but it's really much faster than how it looks here</em></figcaption>
  </figure>
  <br>
  <br>
</div>

* **Lock-free**: Lock-free data structures have significantly higher throughput (no contention) as well as lower latencies as compared to alternatives that use locks under periods of heavy load.
* **Real-Time**: Utilizes Barter-Data with real-time WebSocket integrations enabling the consumption of normalised tick-by-tick data.
* **Multithreaded**: Uses the **[fork-join model](https://en.wikipedia.org/wiki/Fork%E2%80%93join_model)** for delegating non-blocking market event streams into different worker threads.
* **High-throughput**: Uses crossbeam's unbounded MPMC channel under the hood, benchmarked to support _10 million_ market events **per second**.

## Technologies used
- [Tokio](https://crates.io/crates/tokio) ([Tonic](https://github.com/hyperium/tonic) & [Tungstenite](https://github.com/snapview/tokio-tungstenite))
- [Barter-data](https://crates.io/crates/barter-data)
- [Barter-integration](https://crates.io/crates/barter-integration)
- [egui](https://crates.io/crates/egui)
- [futures](https://crates.io/crates/futures)
- [Serde](https://serde.rs/)

## Getting started
Just clone it and run it bro it's easy. No more CMake shenanigans 😊.
```rust
cargo run
```

## 🛣️ Roadmap
- Tracing subscriber for debugging and async-aware diagnostics.
- Notifications (PARTIALLY DONE): See [egui-notify branch](https://github.com/g-tejas/enigma/tree/egui-notify)
- Tabs and Workspace functionality to preserve layouts for traders. [Like this](https://discord.com/channels/900275882684477440/904461220592119849/1012443669451776041) is what I mean.
- Improve multi-threading by delegating and scheduling new jobs to pre-initialized worker thread pool.
- More widgets: Look at the [widget branch](https://github.com/g-tejas/enigma/tree/master/src/widgets) for more deets. (e.g Liquidity heatmap, watchlist)
- Especially this one

https://user-images.githubusercontent.com/76802638/209623672-22191104-5f69-47c7-a359-19326c5f8c14.mp4


## 📚 Resources / Other stuff
- [Naming conventions](https://rust-lang.github.io/api-guidelines/naming.html)
- [Egui navigation: basic centralpanel, layout stuff](https://github.com/mikael-nilsson-github/rust-egui-basic-navigation)
- [Egui, to spawn separate thread for loading data](https://github.com/mikael-nilsson-github/egui-alpaca-crypto-trading)
- [Egui + Reqwest + Tokio + Alpaca](https://github.com/mikael-nilsson-github/egui-async-reqwest-tokio-alpaca/blob/main/src/main.rs)
- [Parasyte Tokio Original implementation](https://github.com/parasyte/egui-tokio-example/blob/main/src/main.rs)
- [Chartbot by SwayStar (but it's not multithreaded)](https://github.com/SwayStar123/chart_bot/blob/master/src/chartbot.rs): For drawing lines on plots and loading data from csv.
