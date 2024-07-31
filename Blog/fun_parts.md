[Resume](../resume_page.md), [Projects](../projects.md), [Blog](../blog.md)

# Microcontrollers

## RP2040 
A really great option when you're looking for something cheap and quick that can be programmed at a plethora of levels. The options that are primarily supported are Micropython, C, and C++; however, I've seen work with rust on it which is always good fun. The dual M0 cores make it suitable for light levels of multi-tasking, especially when paired with a good RTOS to handle the timing itself. The PIO cores can allow for simple state machine like behavior which allows for easier responses at the system clock speed. Generating things like VGA signals, or even DVI signals are then possible. 

Part of the reason I like recommending this chip to students is the USB programming which eliminates the need for any sort of external programmer. This makes it ideal for students who are just getting into embedded systems, or for projects that need to operate on shoe string budgets without access to more experienced individuals. 

## ATTiny 2313
So I used to use AVR microcontrollers fairly extensively in my various small projects. Coming in DIP packages back when I soldered all my projects myself I ended up quite liking these ATTiny chips for their greater number of IO as I seemeed to always find myself IO limited in most designs. I've used a lot of the AVR series at this point with Micros over 100 pins; however, during the early days when TQFP packages made me nevous there was definitely a lot of cases where the DIP 20 package costing ~1/2 that of the lightest ATMega chips was an ideal solution for me.

### W55RP20 
I saw a link saying that this chip will be dropping sometime soon. It's a combination of the RP2040 with the addition of Flash and Ethernet. Making it the ideal single chip solution to create low volume projects which connect up to ethernet. It's definitely something I'll be checking out as soon as I get the chance. 

### P2X8C4M64P
This seems like a good all in one solution. Although coming in at the eye watering cost of $35 per chip! The propeller microcontrollers from parallax are 8 core microcontrollers with enough peripherals and connectivity to choke a horse. I hope I get the excuse to embed one of these into a project at some point. The datasheet quite interestingly has its revision history showing that the chip has undergone multiple revisions since its original release in 2018, with the most recent REV C release coming in 2020 helping with ADC performance marginally. Several of its features seem promising for various applications, although the lack of sufficient details somewhat stops me from pulling the trigger on certain solutions. For instance the Smart I/O pins brag 64 identical pins, but I somewhat have trouble believing that the Triangle/ SawTooth/ SMPS PWM output can be activated differently for every output. 

# FPGAs
I'm quite the Xilinx Fanboy when it comes to FPGAs. I still have yet to integrate one into my own board design; however, that day is certainly coming at some point. I originally learned FPGA programming with the Digilent Basys 3 board containing a Artix 7 FPGA on board. I then got to work with the Zedboard during a chip up and explore the joys of having both ARM cores and FPGA fabric on the same device.

### Renesas SLG47910 
I just put in the request for some sample parts of this 1K LUT FPGA device. If the parts get approved I'll do up a test board for them and see what I can acomplish. The contain a one time programmable non volatile memory for their configuartion. This means they act like very simple ASICs, with a per part cost presumably under a couple of dollars, this makes them a lifesaver where they're required. The 3x3mm package size is ideal for tight spaces where larger custom logic woudln't be doable. Hopefully I can come up with a good project to create with this part to validate a workflow with it once it arrives. 

# Discrete Components
Discrete parts rarely are what one would call interesting; however, every so often I have across a part or two that is intereting simply because it's rare that you get to use it. 

### LSK329A, B, and C
I got to use these parts for a couple of projects and they are certainly interesting as far as discrete parts go. They're matched N-JFET transistors with some exceptionally low noise performance paramters. Down at 3nV/sqrt(Hz) at the 10Hz point. I needed some astonishingly good leakage and flicker noise parameters which is exactly what these transistors provided me. Now if only they didn't cost quite so much at $13/part for the A variant (Best Performance) and $8/part for the C variant (Worse Performance), that being said the specifications for the lower variants include higher-current testing which may be of value. These would make a great low noise analog frontends for a lot of different applications, especially given the GS breakdown voltage of -40V. 

# Very Specific ASICs

## Toaster Controller Chip PT8A2511PE
I really think I want to make a toaster from scratch, and honestly this would be the way I'd want to do it. The chip is relatively speaking fairly simple coming in a DIP 8 package, it is a great way to run a toaster. At $0.76 per chip at small quantities, it is a little questionable if one would be better off saving the passives and using a simple microcontroller to drive some heavy fets to acomplish the same purpose; however, the specific nature of this device likely makes it substantially more durable than it would be if it had to encorporate some form of complicated digital logic.

The chip is simple enough with reasonably functionality that It gives me serious 555 timer vibes having the potential to to acomplish the same level of versatile applications if given the chance. 

## Lightning Sensor AS3935-BQFT
A reasonable looking sensor for detecting lighning within a 40 kilometer radius. I've considered designing this sensor into a camera trigger system for doing better lightning photography. Triggering the camera whenever lightning is detected. Although the sensing would be difficult it would make a great method of capturing awesome photos of lightning strikes assuming that the system can detect fast enough. At $14.43 per chip it's not an insignificant expense; however, the reference design, and built in lightning detection algorithm makes it well worth it.