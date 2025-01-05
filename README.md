
Welcome to GM Chip8 help topic


What is is ?

gm_chip8 is a Chip-8 emulator made under Game Maker 7.0 Professional in January 2025. You can run Chip-8 games under it.

Why did you use Game Maker to make an emulator?

I love the the idea of using not regular software for emulation programming. I even remember when Minecraft players tried making tiny computers under this game with Redstone circuits. Others might say Game Maker is not made for emulation (nor Minecraft ?!). I think they're right, but it's also made for gaming, so it has fast graphics rendering. Since I've already tried coding NES emulators, I tried to make one under Game Maker, but I thought it would be too slow and discarded the idea.

So, what happened, then?

Then, I also remembered I've made a Chip-8 emulator 10 years ago under Visual Basic .NET 2010, and I thought it would be a real engineering feat to test out how it will render under Game Maker. Plus, this software supports binary file loading, arrays, and bitwise operations. So, I took my old Windows XP laptop, opened Game Maker, and here it is: a full Chip-8 emulator that's made under Game Maker 7.0 Professional. This is more a "proof of concept" that anything, but I was not "alone" in this project. There are a lot of online documentation and ChatGPT. I used my former Chip-8 emulator and other emulators to test if the GM one worked, but did not copy a single line of it.

How to use it ?

When the emulator window is ready, simply press the "Open" button and load any .ch8 file into it. The icon is shaped like a folder with an arrow, it's the first one at the top left corner. Then, you may want to click the "Run" icon.

Features

•	Run, pause and stop buttons to control the CPU
•	Toggle debug mode
•	Toggle chip sound
•	Toggle full screen mode (if the window feels too small on your slick brand new 4K screen)
•	Full reset of the emulator
•	Display screen of 256x128 pixels in green and black only (4 times the original Chip-8 display)
•	Status bar that displays emulation state
•	A good old dark green background like in the 90's era.

Tip: Clicking "Run" a second time will reset the emulator.

Keys

1, 2, 3, 4,
A, Z, E, R,
Q, S, D, F,
W, X, C, V.

Are assigned to the Chip-8 pad. No setting available. Plus it only fits the AZERTY keyboard. Keys may not seem responsive, so don't hesitate pushing them a few times.

•	P key will reset the emulator
•	M key will execute instruction by instruction when emulator is paused
•	L key will toggle log mode and write any executed instruction to current folder's "chip8_debug.txt" file. No hexadecimal value (GM does not include an option for that, I had to make a function myself when displaying debug values on screen). Don't forget you activated it, because it may dump huge logs and write to your hard drive in a loop. Logs aren't overwritten but every line is appended at the end of the log, even when you load a new ROM.
•	F4 will toggle full screen mode
•	F9 takes a screenshot of the full window (this is included with GM but I left it)
•	F5/F6 saves and loads the game state (also a GM option, I did not develop it myself)
•	F1 will display the same content that this file
•	ESCAPE will close the window

Debug

GM Chip8 embeds a tiny debugger. If you turn the debugger on, it will display some system values of the Chip-8 under the screen, like PC register, SP register, I address and the last executed opcode. Both PC and latest opcode are displayed in hex values like $FFFF.

Some other debug features like displaying pressed keys were developed but later removed, because it took too much space on screen. The most important values are still displayed.

Game speed

I've set the speed of the window to 60 (the "room"), but I don't know how fast the real Chip-8 runs games. Just remind there are 60 instructions run every second, and I don't know whether there are more or less executed. I've put a greater value but it still runs the same. Hence, GM Chip8 might be running at real speed hardware, and not at a crazy speed like other emulators do.

(Author's note: sorry if the flickering effect will tear your eyes apart)

License

GM Chip8 is an open source project, and comes with no warranty. You use this software at your own risk. For instance, my display driver has already crashed by switching windowed mode and fullscreen mode too fast, making my screen black. But maybe that's because I made the emulator under an old Fujitsu Siemens laptop with an old Windows XP installation. This might not happen to you (at least, I hope so). The chip8.gmk file shipped with the emulator is the full Game Maker project, you may need at least Game Maker 7.0 to open it. That's the whole emulator "source code".

If you don't have Game Maker on your computer, I've left the "gm_chip8_cpu.txt" file that contains the main CPU code, for educational purpose, if you want to read how an emulator is made. GM Chip8 is also shipped with two free ROMs I've made myself under FrHed, they are named "drop.ch8" and "xmas.ch8" that will display a water drop falling from the top of the screen, and christmas bulbs with alternating lights. They're here for demo purpose and can be freely distributed/decompiled.

What's handheld by GM Chip 8 ?

GM Chip8 supports loading regular ch8 files into the emulator (thanks to file binary open mode of Game Maker). It also features all of the Chip-8 opcodes. The RAM is fully implemented, as for the I address register, the included hex digits sprites at the beginning of the RAM (address $0000-$01FF), the PC register also works as well as the RAM stack with the SP register. Even if it's Alpha, I don't remind any issue with the emulation, except the dot moving around without stopping in the Cave game (that's maybe how it's supposed to work...).
GM Chip8 also supports the sound routine, it plays a looped "beep" sound whenever the game calls the sound timer. This is a beep sound included with Game Maker and if it bothers you, you can disable it by clicking on the audio icon in the main toolbar. Delay timer is also supported. Sprite drawing on screen with sprite collision is fully implemented, with the enabled XOR effect (overwriting a lit pixel will disable it).
My former Chip-8 emulator made under VB.NET did handle a few Super-Chip8 opcodes, but this one doesn't, so it will not run Super Chip-8 games at all.

Credits

ChatGPT and online Chip8 documentation (Cowgod). Mark Overmars for the Game Maker project.

Have fun using it and if you enjoy it, thanks for your support ! :-D

By Monokeros (Jan 2025)




