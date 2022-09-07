# Frequently asked questions

### How many sats do I need to open a channel when joining a ring?

Since you also need some sats to open, close and perhaps reopen a channel it is recommended to have at least 40.000 sats in your wallet on top of the amount of sats you need to open your channel. That means if you participate in a 500.000 sats ring, have 540.000 sats in your on-chain wallet.&#x20;

### Why is the channel size of my channel lower than the amount I entered when opening?

In the channel overview of Umbrel, after opening the commit fee is deducted from the full capacity. This is better explained as a reservation of the on-chain fees when the channel is closed unilaterally.

### Why can't I spend or receive the full amount visible on one side of a channel?

A fixed amount (often 1% by default) is reserved on each side on the channel in the case you need to force-close a channel.&#x20;

### What if someone leaves the ring or closes a channel?

The ring is mainly a convenient form of people connecting to each other so everyone participating in a ring ends with two nicely balanced channels (if all goes well of course). 
After that everyone is free to go their own way as they want to. One node might join other rings, another one might decide running a node is not for them and stop alltogether.

### What if the channels of the ring are out of balance?

Being out of balance is actually a good sign, because then you either have a reason to spend sats yourself or you are attractive for routing. 
It is up to everyone to choose their next step themselves. Some people seem very obsessive about continuisly rebalancing but that isn’t necessary and in my opinion often a waste of sats.