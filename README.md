# PeachOS Kernel Security

## Project Overview
PeachOS is a bare-bones operating system derived from repository https://github.com/nibblebits/PeachOS/commit/bc0d8a86197686df9b3ec25ce036508fee412221. This repository is an fork of the nibblebits repoistory to add security features to the design. THis repoisitory focuses kernel level access control, with a focus on file / process authorization and principle of least privelege.

## Features
- Process authorization levels
- File access restrictions
- Filesystem permission checks
- 3 basic file permissions (hardcoded with examples)
- example of the different file permission locks working with terminal output

## Example
Format of the output for the example goes like 
- User permission
- Process of going to blank (a) allow / deny
- Output of secret.txt (x)
- Output of fopen on regular.txt (y)
- Output of hello.txt (z)
- Space between and switch user permission (then repeat_)

## How to Use
first need to download qemu
- sudo apt update
- sudo apt install nasm
- Nasm -v
- sudo apt install qemu-system-x86
- should also install build-essential, bison, flex, libgmp-dev, libmpc-dev, libmpfr-dev, and texinfo
- ./build.sh
- qemu-system-i386 -hda ./bin/os.bin
make sure to be in root directory while doing these commands

# How to run once installed
- after every change do ./build.sh
- then run qemu-system-i386 -hda ./bin/os.bin

