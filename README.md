# Atari 2600 for [MiSTer Board](https://github.com/MiSTer-devel/Main_MiSTer/wiki)

### This is the port of [A2601 by  Retromaster](http://retromaster.wordpress.com/a2601)

### Installation
* Copy the *.rbf file to the root of the system SD card.
* Place some Atari 2600 ROMs into Atari2600 folder

## Usage notes

### Differences from original version
* Joystick/Paddle mode switched by joystick. Press **Paddle1/2** to switch to paddle mode (analog X/Y). Press **Fire** to switch to joystick mode (digital X/Y).
* Keyboard always acts as a joystick. You need to define the keys in joystick menu.
* Video aspect ratio switch in settings menu
* Mouse emulates analog paddles.

### Supported mappers
* Auto detected: F8, FA, F6, F4, F0
* Manual set through file extension(ex: my_game.E0) : E0, FE, 3F 
* SuperChip (128b RAM) must be enabled before load the game if required.

### Original readme
A2601 An FPGA-based clone of the Atari 2600 video game console (Release 0.1.0)

This archive contains source code for VHDL implementation and Python script utilities for the A2601 video game console project.

VHDL source code provided includes implementation of the 6502(7) CPU, the TIA, the 6532 RIOT, additional audio/video/joypad circuitry and bankswitching schemes plus additional RAM used by some game cartridges. Test benches are supplied for all main components (although they may be slightly out of date).

The 6502 CPU core has been developed from scratch for this project. It contains hand-crafted finite state machine and controls that implement all documented 6502 opcodes. It synthesizes quickly and has good performance in the simulator. 

The TIA implementation digitally synthesizes NTSC composite video signal via a lookup table that contains a sequence of values that signifies a sine wave at correct phase for each one of the 16 chrominance values selectable in the TIA. 

You should be able to synthesize the A2601 in Xilinx ISE without any major problems. No project files are included, but it is best to create these yourself, anyway. Two top level entities are provided: One reads cartridge ROM data from on-board flash memory, the other stores the ROM data in the FPGA built-in SRAM. It is also possible to run A2601 sources in a VHDL simulator. Some helper utilities and a test bench are provided for this purpose in the A2601/util directory.

For more information, visit the project website at <http://retromaster.wordpress.com/a2601>.

All source code and other content found in this archive is subject to GNU General Public License Version 3. See the included LICENSE.TXT file for details.

Copyright 2006, 2007, 2010 Retromaster.

## Download precompiled binaries
Go to [releases](https://github.com/MiSTer-devel/Atari2600_MiSTer/tree/master/releases) folder.
