# Moving Volume-Weighted Average Price indicator

Moving Volume-Weighted Average Price (MVWAP) indicator is a significant improvement over the traditional VWAP.

This *Moving* VWAP indicator has a user-adjustable sliding window width. Unlike traditional anchored VWAP—whose growing lookback gives every reading a different sample size, this averages a constant number of bars - so readings stay comparable across time.

Traditional VWAP seems useful for traditional securities trading with limited trading hours, but even then one soon realizes that it is hyper-sensitive early in the day - and then nearly completely insensitive by the end of the day; thus being practically useless, even though the concept is appealing.

This is especially evident for cryptocurrency, which has no "start" or "end" to trading.

By instead using a moving average (of a constant but user-definable) width, all values throughout the day mean exactly the same thing.
