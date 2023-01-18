# Getting Started

Okay, enough talks. Now let's see how quisp is working with our bare eyes. We have to build QuISP in our machine for that.

> :warning: **Building the software from source** might look awkward to some developers with interpreter-based languages (such as Python, Lua, JS...). We are going to add the software build section to the textbook, explaining the architecture of GNU `make` and the concept of `makemake` we are using with OMNeT++. Don't switch the channel! For now, you can follow our manual to get the correct result.

## Installation

### Recommended Environment
- Docker with at least 6GB of allocated RAM (you can change that in Docker Desktop Settings)
...and that's it!

The following procedures were confirmed working on the MacOS Catalina (10.15.3) and Mojave(10.14).

### TL;DR
- Install brew, docker, XQuartz and socat with `sh docker_tools.sh`
- clone quisp
- `docker pull ghcr.io/sfc-aqua/quisp`
- Run docker with `sh docker_run.sh`
- Run `omnetpp` command on the docker container

---

### Automated way

1. Open your terminal and run

```zsh
$ git clone https://github.com/sfc-aqua/quisp.git
```

You can download quisp from github.
Enter quisp with `cd quisp`
2. Run shell script

```zsh
$ sh docker_tools.sh
```

After you have successfully installed the related tools, please reboot your laptop. (Maybe just rebooting your terminal is enough.)

3. Build docker container

Open terminal and run,

```zsh
$ docker pull ghcr.io/sfc-aqua/quisp
```

A docker image called quisp should have been created. You can check with the command `docker images`.

4. Run docker container

OK, now you can enter the container.

```zsh
$ sh docker_run.sh
```

If this error pops up,
```zsh
docker_run.sh: line 15: xhost: command not found
docker_run.sh: line 15: xterm: command not found
```
add `/usr/X11/bin` (might vary) to your path

5. Try quisp!

If all of the processing completed successfully, you should see

```zsh
quisp:/root/quisp$
```

Open omnet with

```zsh
quisp:/root/quisp$ omnetpp
```

Enjoy quisp!

