# blinkt_ragnet_monitor
A script for your Pimoroni blinkt that displays a RED / AMBER / GREEN Value on LED 7 (closest LED to USB ports).

![img](https://github.com/tomweston/blinkt_rag_monitor/boot_blinkt.gif)

Code adapted from: 

https://github.com/randomInteger/blinkt_internet_monitor
&
https://github.com/pimoroni/blinkt

Install into "/home/pi/Pimoroni/blinkt/examples" after installing blinkt from
the link above.

Launch on boot by adding the following to "crontab -e":    
@reboot python /home/pi/Pimoroni/blinkt/examples/ragnet_monitor.py &

Kill via shutdown script with:    
pgrep -f /home/pi/Pimoroni/blinkt/examples/ragnet_monitor.py | xargs kill -SIGINT

Tested on Rpi3 with Pimoroni blinkt with Raspbian GNU/Linux 8 (jessie).

This script catches SIGINT to shutdown cleanly so the LEDs do not stay lit when the OS is in shutdown.
