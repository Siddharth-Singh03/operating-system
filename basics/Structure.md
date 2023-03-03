
# Structure types
- Simple 
- Monolithic
- Layered
- Micro kernal
- Modular



## Simple
- every component had access to every other component
- because of this data was not safe
- it was an old structure
- any error can curropt the whole system.
- E.g. - MS Dos (Intel 8088)



## Monolithic
- All system functions are clubbed into single layer
- number of users = number of shells
- shell take care of any errors and acts as command interpreter, after solving it will transfer it to kernal
- users or any layer does not interact directly with the hardware.
- E.g. - Unix OS(fedora)

DISADVANTAGE 
1. to make any changes we have to modify the kernal completely.


## layered 
- OS is broken into number of layers
- the bottom layer (layer 0) is the hardware, the highest layer (layer n) is the user interface
- to make any changes only that layer has to be modified.
- hardware is protected by many layers
- E.g. - Windows NT

DISADVANTAGE -> 
1. upper layer gets services from lower layer but lower layer doesn't get services from upper layer; so fixing which layer should be above or below becomes difficult.

2. If layer n wants to access layer 1, then it has to pass through all the layers which is time consuming.
## Micro kernal
- removes all non essential components from the kernal and implementing them as system and user level programs.
- provides minimal process and memory management in addition to a communication facility.
- micro kernal only have core functionality while other are built on user mode
- design, implementaion and error correction are very easy
- gives command access to client/user program and system files
- E.g - L4 Linux, Mac OS

DISADVANTAGE ->

1. communication takes place through pipes/message passing, hence this becomes slow.
## Modular
- Hardware is in between and programs are stored as separate modules
- object oriented programming techniques were used to design operating system
- If any modules wants to access hardware it can do so without passing thorugh other modules
- No message passing takes place hence the process is fast
- E.g. - Windows 7 and above