# Compiling

You have several options for compiling.

## Cross-compiling

You can use a cross-compiling toolchain to create ARM compatible code. Note: You need a Linux toolchain,
not a "bare-metal" toolchain. If it does not have "linux" in the name, it probably won't work.

Pros: Fastest option. Works on Windows and Mac without a virtual machine.

Cons: Only includes standard libraries - no Debian `-dev` packages.

### Windows

[MentorGraphics toolchain](http://sourcery.mentor.com/public/gnu_toolchain/arm-none-linux-gnueabi/arm-2014.05-29-arm-none-linux-gnueabi.exe) (formerly known as CodeSourcery).

### Mac

[Carlson-Minot toolchain](http://www.carlson-minot.com/available-arm-gnu-linux-g-lite-builds-for-mac-os-x/mac-os-x-arm-gnu-linux-g-lite-201405-29-toolchain)


## Brickstrap

Brickstrap uses QEMU to create a virtual environment (not exactly a virtual machine) that can run the same ARM
compatible code on a different type of computer.

Pros: Faster than running on the EV3 itself. Can install all Debian `-dev` packages using `apt-get`.

Cons: Slower than cross-compiler. Requires Linux (Ubuntu).

See [this page](https://github.com/ev3dev/ev3dev/wiki/Using-brickstrap-to-cross-compile-and-debug) for instructions.


## On the Brick

It is possible to compile programs on the EV3 brick itself.

Pros: Easy to setup.

Cons: Really slow.

Just run `sudo apt-get install build-essential` on the EV3 and you will have everything your need.
