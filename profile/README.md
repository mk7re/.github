# Mario Kart 7 Reverse Engineering

## Useful links
- Additional header documentation:
   * https://github.com/PabloMK7/EveryFileExplorer/tree/master/MarioKart/MK7
   * https://github.com/PabloMK7/CTGP-7_Open_Source/tree/main/Includes
   * https://github.com/kinnay/NintendoClients/wiki/NEX-Protocols

- [How to access our shared Ghidra repository](https://imgur.com/a/N30GCJA)
- [Symbol maps for the Download Play child executables](https://tcrf.net/images/8/89/MK7_Download_Play_Child_Symbol_Maps.zip)
   * Additionally, you can find [the symbol maps for Nintendogs + cats here](https://tcrf.net/images/a/a4/NintendogsCats_Symbol_Maps.zip).<br>
     Both *Nintendogs + cats* and *Mario Kart 7* use the same engine, and because the symbol maps for *Nintendogs + cats* are for the full game, it reveals some symbols not present in the *Mario Kart 7* DLP symbol maps.
- [Custom Mario Kart 7 Wiki (File Format documentation)](https://mk3ds.com/)
- [decomp.me preset with decompiled functions](https://decomp.me/preset/194)
- [List of various tools for modifying the game's assets](https://docs.google.com/document/d/1iXHI7zIWe7g7o8QMUUqdBQCS7k8uOUq4QWMs5rU0JdQ/edit?tab=t.0) (courtesy of Cats4Life from the CTGP-7 server)
- [Useful notes, speadsheets and others](https://drive.google.com/drive/folders/1SA4hMsJw4gPiC0jozNVZQnm6fIZsNPUW?usp=drive_link). Additionally, [check this page out for more notes](https://tcrf.net/Notes:Mario_Kart_7).
- [Vehicle-related notes](https://docs.google.com/document/d/1OHsHC0NAbHimsyQz4msn3q66pZ0ti8HgL1tEv5Kj15U/edit?tab=t.0)
- [General tutorial for 3DS game modding and reverse engineering](https://gamebanana.com/tuts/13395)

- Related Discord servers:
   * [Mario Kart 7 TCRF](https://discord.gg/RAcJShncQ4)
   * [CTGP-7](https://discord.com/invite/0uTPwYv3SPQww54l)
   * [3DS Game Decompilation](https://discord.gg/dFgw7CwrEX)

## Misc. notes
### Debugging
Mario Kart 7 can be used alongside a debugger in both a real 3DS with Luma CFW (recommended), or an emulator capable of connecting to a debugger client. [More info](https://bmaupin.github.io/wiki/other/3ds/3ds-debugging.html).

* If using IDA: It's best to use IDA Pro version 7.0, as the debugger in this version is less likely to have issues with breakpoints and other elements while debugging. Note that, if using an emulator, there's a chance that you won't be able to write data to memory nor registers using the debugger cleint.
* If not using IDA: devkitARM's own gdb debugger client should work fine, though we personally recommend using [gdb-multiarch](https://packages.msys2.org/packages/gdb-multiarch?variant=x86_64) via WSL or MSYS64 (if using Windows). If using an emulator to debug, ensure to write the statement `set architecture armv7` after opening GDB so that it knows the architecture we're going to debug is ARM specifically.
