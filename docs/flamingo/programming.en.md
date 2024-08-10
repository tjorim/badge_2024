# Programming the LANA Module
To program the blaster (flamingo) you can use [Mounriver Studio](http://www.mounriver.com/) IDE or [Embeetle](https://embeetle.com/). 

## WCH Official tools
[Mounriver](http://www.mounriver.com/) is an ide based on eclipse released by the chipmaker WCH. This works on Windows and there is a version for linux and possibly also for Mac, but the last 2 are a bit behind. [Mounriver](http://www.mounriver.com/) also gives false reports of viruses on many systems and violates the GPL license conditions of Eclipse.

## Embeetle
A nicer alternative is [Embeetle](https://embeetle.com/). this is an IDE of Belgian make. This is not open source but does produce an open toolchain when creating a new project.

[LANA](https://phyx.be/LANA_TNY/) can be programmed with [Embeetle](https://embeetle.com/) via the USB connector but also with the [WCH-Link debugger]
(https://www.wch-ic.com/products/WCH-Link.html), this gives extra debugging options.

The makers of [Embeetle](https://embeetle.com/) have also been so kind to [add the LANA board and very nice documentation](https://embeetle.com/#supported-hardware/wch/boards/lana-tny-01).

## Notes on LANA module
If you are going to work with the blaster/LANA TNY yourself, you have to pay attention to 1 thing (regardless of the IDE) that is that LANA does not have an external clock and must use the internal clock (HSI), this is also stated in the default sketch of [Embeetle](https://embeetle.com/).
If you accidentally "brick" your [LANA](https://phyx.be/LANA_TNY/) board, you can usually unbrick it via USB or by using the power reset feature of the [WCHISPTool](https://www.wch-ic.com/downloads/WCHISPTool_Setup_exe.html).
