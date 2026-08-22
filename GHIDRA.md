# Accessing `mk7re`'s shared Ghidra project

We have a [Ghidra](https://github.com/nationalsecurityagency/ghidra) project that hosts code and documentation for different versions of `Mario Kart 7`'s executable. It is hosted by the hosted by the [GC / Wii decomp Ghidra server](https://discord.com/invite/hKx3FJJgrV).

## How to access
1. Register at https://ghidra.decomp.dev/ with your Discord account, then set a password for accessing the Ghidra repo.
Once you do this, select the `mk7` repository, and select the Role you would like to have (Read, Write or Admin), then hit "Request".
2. In Ghidra, select File > New Project > Shared Project. On "Server Name" (Hostname) and "Port number" (Port), set the information from the "Connection Information" that appears in the link above once you've logged in.
3. If done correctly, you should see the `mk7` repository under the "Existing Repository" box, select that and click Next, then click Next and Finish on the following screens.

**Make sure you use Ghidra v11.4 specifically for this repo.**

## Contents
In the root directory, you will find the following executables:
* `CHN_Rev1`: Simplified Chinese (iQue) version.
* `E3_2010`: E3 2010 version.
* `EUR_DP`: European Download Play version. **This is the file that has the most documentation on overall, but it's missing some code not in the retail versions.**
* `EUR_Kiosk`: European Kiosk demo.
* `EUR_Rev0`: European Rev0 version (v1.0 without any patches).
* `EUR_Rev0_v1.2`: European Rev2 (1.2) update.
* `KOR_Rev1`: Korean Rev1 version.
* `USA_Rev0_v1.1`: American Rev0 (1.0) version with the v1.1 update.
* `USA_Rev1`: American Rev1 version (USA v1.1, prepatched). **This file has the most documentation on code that's only present in the retail versions.**

In the References directory, you will find these files:
* `Bowling3DS.axf`:  This is a debug version of the executable from the Brunswick Pro Bowling game. It contains all function names, class names, and the classes are all properly filled out, thanks to leftover DWARF data.
* `NintendogsCatsShiba_Korean`: This is the executable file from the Korean version of the Nintendogs+cats Shiba edition. Nintendogs+cats shared various parts of the engine with MK7, since both were developed by the same dev team pretty much.
* `NintendogsCats_E3_2010` is the executable obtained from the E3 2010 build of Nintendogs+cats. Like with the final version of the game, this build also shares several parts of the code with the E3 2010 build of MK7.
* `TriforceHeroes_EUR_DP_Debug`: This is the code.bin for the [Debug version of the Triforce Heroes DLP](https://tcrf.net/Proto:The_Legend_of_Zelda:_Tri_Force_Heroes/Download_Play_Debug_Build), another 3DS game that uses the `sead` library.