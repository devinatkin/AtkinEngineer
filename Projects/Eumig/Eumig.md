This is in progress. If you found this page turn around...
[Work With Me](resume_page.md) [Projects](projects.md), [Blog](blog.md)

I have a Eumig Viennette 3 Super 8 Camera which I quite like the feeling of. It has taken nice videos when I've used it in the past, and I really want to continue using it. I'm not some hipster idiot. I just like the feel of the analog camera, the level of thought required to get shots worth taking, and frankly I'm in front of the computer enough that the idea of shooting on super 8 simply to avoid living permanently on a computer is enough. I got the camera initially on vacation when we found it in an antiques store. It was cheap, and came with a roll of unshot film (Kodachrome so no point in shooting it without a friend whoose very into doing complicated chemsitry). It didn't work to begin with because, first the film was inserted the wrong way around..., and second more annoyingly the battery holder was gone. 

It is supposed to run on 6AA with a small plastic piece that presses into the top contacts to run the device. It has battery detection and all that fun stuff so that you can tell when your system is going to die in advance. My first fix was admitedly very crude with only a simple boost converter, charger, and lithium ion battery wired up and crammed into the battery compartment. This lasted well enough for a few rolls and got it through the wedding we wanted to shoot it at. But it didn't do so well when we took it to the zoo and an unfortunate clip the a wire led to the battery shorting and the compartment almost catching fire. It was all removed in time that the damage to the camera was essentially nill (A small melted hole near the bottom where the wire was crimped out). 

I obviously want to fix the device up again, so here's the plan. 

### Requirements
- It's gotta take a lithium ion battery (2AH 3.7V is sufficient and fits nicely in the compartment)
- It's got to have low voltage cut-off to prevent over discharging the cell and damaging the pack.
- It's got to have a setup to 9V, optionally if possible it would be cool to mimic the curve of a 6 AA batteries so that the battery monitor on the camera could work
- It's got to have USB charging, ideally on a thin little wire that can be run out of the camera for easy charging when not using the battery.
- For Debugging Purposes I'd like to have charging and discharging leds.

I haven't looked into this deeply yet but I'm thinking possibly using an RP2040 as a battery management system. Using the single cell given a starting voltage of 4.2V and a minimal voltage of 3.5V (Well above the damange point), a simple boost converter could control the voltage effectively to either allow the system to run or not. The only thing missing would then be to include a simple 1 chip solution for the charging.

### Dimensions
Gotta Grab these 

### Schematic Design

### Final Layout

### Fabricated Board

### First Roll