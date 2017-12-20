# FHeroes2 port for PS Vita
## Building
### Prerequisites
- libSDL2 (libSDL1 works, but performance is far superior with second one)
- libSDL2-mixer (optional, but sound is corrupted without it in libSDL2 build)
- libSDL2-image (optional)
- libSDL2-ttf (optional, but required for translations)

To build the game just run
```
make -f Makefile.vita
```

## Original data
FHeroes2 requires data files from the original Heroes of Might and Magic 2.

Copy HEROES2.AGG and HEROES2X.AGG (if you own Price of Loyalty expansion) from the original games DATA folder to the ux0:data/fheroes2/data and everything from MAPS folder into the ux0:data/fheroes2/maps.

Data from GoG version of the game is working nicely. Files from the demo version should work too.

Music files in OGG format should be placed into the ux0:data/fheroes2/files/music/ folder.

In order to get music working with audio from GoG release, some file renaming is required (at least with my version of the game).

- homm2_01.ogg -> 02 Battle (1).ogg
- homm2_02.ogg -> 03 Battle (2).ogg
- homm2_03.ogg -> 04 Battle (3).ogg
- homm2_04.ogg -> 06 Sorceress Castle.ogg
- homm2_05.ogg -> 07 Warlock Castle.ogg
- homm2_06.ogg -> 09 Necromancer Castle.ogg
- homm2_07.ogg -> 10 Knight Castle.ogg
- homm2_08.ogg -> 05 Barbarian Castle.ogg
- homm2_09.ogg -> 08 Wizard Castle.ogg
- homm2_10.ogg -> 11 Lava Theme.ogg
- homm2_11.ogg -> 12 Wasteland Theme.ogg
- homm2_12.ogg -> 13 Desert Theme.ogg
- homm2_13.ogg -> 14 Snow Theme.ogg
- homm2_14.ogg -> 15 Swamp Theme.ogg
- homm2_15.ogg -> 16 Ocean Theme.ogg
- homm2_16.ogg -> 17 Dirt Theme.ogg
- homm2_17.ogg -> 18 Grass Theme.ogg
- homm2_18.ogg -> 19 Lost Game.ogg
- homm2_19.ogg -> 20 Week (1).ogg
- homm2_20.ogg -> 21 Week (2) Month (1).ogg
- homm2_21.ogg -> 22.ogg
- homm2_22.ogg -> 23 Map Puzzle.ogg
- homm2_23.ogg -> 24 Roland's Campaign.ogg
- homm2_24.ogg -> 25.ogg
- homm2_25.ogg -> 26.ogg
- homm2_26.ogg -> 27.ogg
- homm2_27.ogg -> 28.ogg
- homm2_28.ogg -> 29.ogg
- homm2_29.ogg -> 30.ogg
- homm2_30.ogg -> 31.ogg
- homm2_31.ogg -> 32.ogg
- homm2_32.ogg -> 33.ogg
- homm2_33.ogg -> 34.ogg
- homm2_34.ogg -> 35.ogg
- homm2_35.ogg -> 36.ogg
- homm2_36.ogg -> 37.ogg
- homm2_37.ogg -> 38.ogg
- homm2_38.ogg -> 39.ogg
- homm2_39.ogg -> 40.ogg
- homm2_40.ogg -> 41.ogg
- homm2_41.ogg -> 42 Main Menu.ogg
- homm2_42.ogg -> 43.ogg

### Custom maps
You can download some custom map packs here: https://sourceforge.net/projects/libsdl-android/files/FreeHeroes2/

## Configuration
If you want to change game options (like resolution, audio settings, movement speed or translation), copy fheroes2.cfg from ux0:app/FHOMM0002/ to the ux0:data/fheroes2 and edit it.

960x544 resolution is supported, but performance isn't that good with it (especially during combat).

## Controls
- Left analog stick - Pointer movement
- X button - Left mouse button
- O button - Right mouse button
- D-Pad - Map scrolling

To change pointer movement speed edit fheroes2.cfg (copy it from ux0:app/FHOMM0002/ into the ux0:data/fheroes2/ first) file and change vita_pointer_speed variable.

Touch controls are supported. To change touch control type or speed edit vita_touchcontrol_type and vita_touchcontrol_speed variables in fheroes2.cfg file.

- 0 - touch disabled
- 1 - tap mode touch control (default one)
- 2 - offset mode touch control

To divide an army unit press and hold on it and drag the cursor to the empty cell.

## Original port
https://sourceforge.net/projects/fheroes2/
