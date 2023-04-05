# Getting Started

Okay, enough talks. Now let's see how quisp is working with our bare eyes. We have to build QuISP in our machine for that.

> :warning: **Building the software from source** might look awkward to some developers with interpreter-based languages (such as Python, Lua, JS...). We are going to add the software build section to the textbook, explaining the architecture of GNU `make` and the concept of `makemake` we are using with OMNeT++. Don't switch the channel! For now, you can follow our manual to get the correct result.

## QuISP on Linux
### Prerequisites
There are many ways to install QuISP, and you can find all of them on the wiki of QuISP repository. However, we're going to stick to the native installation on linux in this tutorial. When this method is not working, don't panic...you can always use our docker container. If you are just interested in **using** quisp to try some simulations and **not** interested in the building mechanism of QuISP, you can simply use the docker container to save your time.  

First, please install `clang` on your system. It is widely available on the various Linux package managers, so it should be very simple like: `sudo pacman -S clang` or `sudo apt install clang`.  

Second, install the OMNeT++, which is the DES (Discrete Event Simulator) we are using to run QuISP. Refer to the following PDF guide to get the instructions for installing QuISP, and get back here when it's done. We recommend you to prepare a cup of coffee, tea, or anything you prefer, since it might take your time a bit.  

<embed src="https://doc.omnetpp.org/omnetpp/InstallGuide.pdf" type="application/pdf" width="100%" height="50%">

If `clang` is availabe in your system and you can run the OMNeT++ executable `omnetpp` from your terminal emulator, you can proceed to the next step.

### Building the QuISP
To build QuISP, you should get the source in your working directory by cloning our repo and `cd` inside the directory:  
```bash
$ git clone https://github.com/sfc-aqua/quisp && cd quisp
```   
Now we are in the cloned repository.  
You will see a `Makefile` in the root of our repository, but now is not the right time to trigger `make` here. There is **one more** `quisp` directory inside the repository, and that is where the most of our core logic source codes live. This might cause a bit of confusion, so from now on I will always write their locations in a following form: `quisp/` and `quisp/quisp/`.

