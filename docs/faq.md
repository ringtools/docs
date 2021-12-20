# Frequently asked questions

### How many sats do I need to open a channel when joining a ring?

Since you also need some sats to open, close and perhaps reopen a channel it is recommended to have at least 40.000 sats in your wallet on top of the amount of sats you need to open your channel. That means if you participate in a 500.000 sats ring, have 540.000 sats in your on-chain wallet.&#x20;

### Why is the channel size of my channel lower than the amount I entered when opening?

In the channel overview of Umbrel, after opening the commit fee is deducted from the full capacity. This is better explained as a reservation of the on-chain fees when the channel is closed unilaterally.

### Why can't I spend or receive the full amount visible on one side of a channel?

A fixed amount (often 1% by default) is reserved on each side on the channel in the case you need to force-close a channel.&#x20;