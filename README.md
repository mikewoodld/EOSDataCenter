# EOSDataCenter
Documentation for Mike's EOSDataCenter Raspberry Pi Project

This is a working document to keep track of progess on this project. 

EOSDataCenter (working name, needs a better title one day) is a Raspberry-Pi based solution to fetch data from various public and private APIs and return those over a network to an ETC Eos Family Console using OSC. 

Originally inspired by my HockEOS project, EDC currently supports

- HockEOS
- Live Weather
- Places
- MTA Train Times


Eventually the goal is to make this repo into a step-by step how to, as well as documentation on all of the various things that are possible to do with EDC.

# Hardware
- Raspberry Pi
- 4-Line LCD Screen
- Network with Internet Connection
- Network with Lighting Connection
- EOS Family Console (or Nomad)

# Configuration
EDC uses both NICs of a Raspberry Pi. In testing, I've used Wifi for internet and Ethernet for lighting network, but it will work in the opposite direction OR only on one NIC if your network isn't segregated. 

Currently, you must have a DHCP server on at least one of your two networks in order to assign EDC an IP address. 

Once EDC has a valid IP on either NIC, that IP will be presented on the LCD screen. You can then use the configuration tool by navigating to that IP address in a web browser. 

## EDC Configuration Utility
The Configuration Utility appears once you've connected to EDC via a browser.

(Image Here)

You can see your current settings, download your current configuration, upload a backup, or create a new config file using this web browser tool. 

### Connecting to EOS
In the configuration utility, you tell EDC the IP address of your EOS console, as well as the incoming/outgoing OSC ports of the console itself. You do not need to specify ports for EDC, as it will assign itself the necessary ports based on your EOS settings. 

In the utility, you also can turn on/off individual modules. Of course, you choose to display what information you want by creating magic sheet objects, but disabling modules helps to limit the amount of OSC data being sent to EOS as well as takes some load off of EDC.




# The Available Modules:


## HockEOS

Right now, I'm going to leave all of the HockEOS documentation over at https://github.com/mikewoodld/HockEOS. 

## Live Weather

https://github.com/mikewoodld/EOSDataCenter/tree/master/Weather

## Places

https://github.com/mikewoodld/EOSDataCenter/tree/master/Places

## MTA Train Times

https://github.com/mikewoodld/EOSDataCenter/tree/master/MTA
