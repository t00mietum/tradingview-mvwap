<!-- markdownlint-disable MD007 -- Unordered list indentation -->
<!-- markdownlint-disable MD010 -- No hard tabs -->
<!-- markdownlint-disable MD033 -- No inline html -->
<!-- markdownlint-disable MD055 -- Table pipe style [Expected: leading_and_trailing; Actual: leading_only; Missing trailing pipe] -->
<!-- markdownlint-disable MD041 -- First line in a file should be a top-level heading -->
<div align="center">

[![License: MPL 2.0](https://img.shields.io/badge/License-MPL_2.0-brightgreen.svg)](https://opensource.org/licenses/MPL-2.0)
![Lifecycle: Stable](https://img.shields.io/badge/Lifecycle-Stable-brightgreen)
![Support](https://img.shields.io/badge/Support-Maintained-brightgreen)
![Status: Passing](https://img.shields.io/badge/Status-Passing-brightgreen)

</div>

<!-- TOC ignore:true -->
# Moving Volume-Weighted Average Price indicator

t00mietum's Moving Volume-Weighted Average Price (MVWAP) indicator is a significant improvement over traditional VWAP.

## Feature summary

This is a true Volume-Weighted Average Price line, calculated with a predictable, user-definable fixed-width continuously sliding moving window.

It also includes a band of percentage points above and below the center line. (With a user-definable % and can be turned off.) This is super-useful for:

1. "Breakout" confirmation signals

1. visually and mentally adjusting to the true magnitude of price swings, when viewing an automatic scale on the price axis, especially at varying time resolutions.

Optional Volume-Weighted "Bollinger Bands" are also included. (With user-definable window and stddev.) Off by default.

## More detail

The major flaw in TradingView’s built-in VWAP indicator, is that it has a daily reset period that you can’t override, and the volume denominator is cumulative until the next hard reset.

That’s problematic as a reliable technical indicator, because:

1. Throughout the trading day, for literally every bar, the indicator means something different. Since the day’s starting window is so short, it follows price very closely.

1. Then as the day progresses and the denominator gets ever-more huge, the line gets more sluggish. It gradually flattens out and by the end of the day, it may turn completely flat and unresponsive to any price change - which is completely useless. (In other words, the averaging window ranges from 1 bar, to however many bars are in your day - i.e. 288 for a 5-minute view in a 24/7 market.)

1. When the trading day resets - even for 24/7 markets like crypto - the average line usually makes a jarring jump up or down - when volume sensitivity instantly switches from ultra-dull, to 1:1 hyper-sensitive.

This indicator fixes all of those problems, by using a user-definable moving window for the averaging. At it’s core, the center-line behaves just as you would expect from a volume-weighted SMA, no surprises.

As of the publish date, there is at least one other custom, true VWAP indicator available. What sets this apart, is that it also mimics two other would-be great features of TV’s VWAP: A percentage points channel above and below the average line, and a pseudo Bollinger Bands channel. ("Pseudo" because it’s volume-weighted - and so while the math is the same, it’s technically not exactly the same).

## Use it in TradingView

Find it online [here](https://www.tradingview.com/v/YGq2eMZN/), favorite it, then add it to your chart.

## History

- 2025-05-13: First published on TradingView.

- 2025-05-10: Update.

## Copyright and license

> Copyright © 2025-26 t00mietum (CryptogID: ปʬϝღถɔ4რఠΔթะ9ƾǝu) (aka TradingView's "NeanderTraderBC")<br />
> Licensed under the [Mozilla Public License 2.0](https://mozilla.org/MPL/2.0/). No warranty.
<!--
> Licensed under the [MIT License](https://mit-license.org/). No warranty.
> Licensed under the [GNU General Public License v2.0](https://www.gnu.org/licenses/gpl-2.0.html). No warranty.
> Licensed under the [GNU General Public License v2.0 or later](https://spdx.org/licenses/GPL-2.0-or-later.html). No warranty.
> Licensed under the [GNU General Public License v3](https://www.gnu.org/licenses/gpl-3.0.en.html) license. No warranty.
> Licensed under the [Mozilla Public License 2.0](https://mozilla.org/MPL/2.0/). No warranty.
-->