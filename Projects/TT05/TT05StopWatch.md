---
layout: default
---
[Resume](..\..\resume), [Projects](..\..\projects), [Blog](..\..\blog)

# TT05 StopWatch Basic Test

![PMOD Stopwatch Board](PMOD_Board.png)
I prepared this PMOD board and am having it fabricated with JLCPCB in order to effectively test my Tiny Tapeout 5 design. This design was primarily part of an educational effort and I'll likely be writing about it in more detail elsewhere down the road; however, I'll make sure to link back to here if that does indeed end up occuring. Without the PMOD it's quite annoying to test this design as it's based off of code that's intended to be run on the Basys 3 Board, and therefore has active low outputs for the anodes, and for the cathodes. With JLCPCB being as fast as it is to fabricate boards. This is a lot simpler, although more expensive to complete the testing. 

## Initial Breadboarded Design
Borrowing a 7 segment from the makerspace I was able to validate that the design works.
Here is a video demonstrating the initial breadboarded test: [link](https://youtu.be/YOzGE1vvptc). As you can see the anode order isn't correct; however, this isn't important for the actual functionality as that's a wiring issue related to the fact I only have a 3-digit 7 segment display and am mainly interested in verifying functionality overall while I wait for my pmod design to arrive. . 