- [About](#about)
- [Last changes](#last-changes)
- [Features](#features)
- [Compatibility](#compatibility)
- [Screenshots and Videos](#screenshots-and-videos)
  - [Video View](#video-view)
  - [Elementflix View](#elementflix-view)
  - [Main Screen](#main-screen)
  - [Game List](#game-list)
  - [Menu](#menu)
- [About Auto Collection Logos](#about-auto-collection-logos)
  - [What are collections?](#what-are-collections)
  - [Currently supported franchises](#currently-supported-franchises)
- [Supported Platforms](#supported-platforms)
- [License](#license)
- [Made With](#made-with)


# About

![Version 1.230514](https://img.shields.io/badge/Version_1.230514-de3e80?style=for-the-badge)
![Revision 0.1](https://img.shields.io/badge/Revision_0.1-4CAF50?style=for-the-badge)

> :warning: **EXPERIMENTAL FORK**: This is a personal fork specifically designed for R36Max devices with 1:1 (720x720) square ratio support and minor UI adjustments. This fork is experimental and should only be used for testing purposes. For stable usage, please use the original Elementerial theme.

This is a port in progress for ArkOS.

Elementerial is a theme built totally from scratch for EmulationStation.
It's based on Android TV's interface using some principles from Material Design with the addition of ElementaryOS color palette.

> This theme supports custom backgrounds. Read [CUSTOMBG.md](CUSTOMBG.md) for more details.
> 
> I made an web app to load, crop and save images named as the designated system.
> It's not powerful as Photoshop or GIMP, but help collect a lot of images and download them in one go.
> 
> Access [Albedo Wallpaper Cropper](https://albedo-wallpaper-cropper.vercel.app).
> 
>  If you're concerned about privacy, this web app will never collect or send any information anywhere. The images loaded are saved locally on the browser database. As an web app, it can be used offline after the first load.

<br>

:warning: **Elementerial now plays videos when browsing systems or games, however Elementerial does not come with any videos. You need to use https://www.screenscraper.fr/ or alike to get the videos and then Elementerial will be able to play them.**

<br>

# Last changes
```
v0.1 - Fork Enhancements:
- Added complete 1:1 (720x720) square ratio support for R36Max devices
  * Created view-system-11.xml with optimized layouts for square screens
  * Added ratio11 asset directory with 720x720 background images
  * Fixed status bar positioning and battery indicator alignment
  * Integrated 1:1 ratio option into theme selection system
- Fixed PNG asset format issues (converted from 8-bit colormap to RGBA)
- Added comprehensive .gitignore to exclude IDE files and system files
- Updated compatibility documentation for square ratio devices
- Forked from original Elementerial project for ArkOS optimization

```

<br>

# Features

This theme has 14 color schemes:

* Strawberry (Red)
* Orange
* Banana (Yellow)
* Lime (Green)
* Mint (Turquoise)
* Blueberry (Blue)
* Grape (Purple)
* Bubblegum (Pink)
* Cocoa (Brown)
* Slate (Gray)
* SNES Scheme (based on the SNES aged carcass color. Yellowish Gray + Purple)
* Gameboy (based on the GB carcass. Gray + Claret + Green)
* Pikachu Edition (based on the GB Pikachu Edition. Vibrant Yellow + Blue + Red)
* Red Fruits (just a fancy color combination. Blue + Red + Purple)

And 2 styles:
* Dark
* Light

Selectable text sizes:
* Small
* Medium
* Large

<br>

# Compatibility

This fork is developed for RG353V running ArkOS.

Original Elementerial was made for the following resolutions:

- **480x320** (3:2 screen ratio), tested on Anbernic RG351M running AmberElec and RetroBat
- **640x480** (4:3 screen ratio), tested on VirtualBox running Batocera and RetroBat
- **1920x1152** (5:3 screen ratio), tested on VirtualBox running Batocera and RetroBat
- **720x720** (1:1 screen ratio), tested on R36Max running ArkOS

\* It's possible to use Elementerial in other resolutions and systems based on EmulationStation, however full compatibility is not guaranteed.

<br>

# Screenshots and Videos
## Video View
https://user-images.githubusercontent.com/57257682/229651591-5ea370f6-df3a-437e-b422-6f531fd50e45.mp4

## Elementflix View
https://user-images.githubusercontent.com/57257682/229651681-24c01dc0-fa6b-4f80-b13e-3e5d797f486e.mp4

## Main Screen
| ![](https://i.imgur.com/smncxP7.png) | ![](https://i.imgur.com/qDWQhaB.png) |
| :----------------------------------: | :----------------------------------: |
|          Strawberry + Dark           |       Pikachu Edition + Light        |

## Game List
| ![](https://i.imgur.com/7aPxKvO.png) | ![](https://i.imgur.com/ADsrJET.png) |
| :----------------------------------: | :----------------------------------: |
|     Mint + Dark + Detailed View      |   SNES Sheme + Light + Boxes View    |

## Menu
| ![](https://i.imgur.com/rXcTHq0.png) | ![](https://i.imgur.com/F8b0CXZ.png) |
| :----------------------------------: | :----------------------------------: |
|           Blueberry + Dark           |       Game Boy Scheme + Light        |

<br>

# About Auto Collection Logos

Elementerial now show logo for some auto/custom collections.

## What are collections?
Collections are a way to arrange your games.
You can create editable or dynamic collections.
Editable collections are those you manually add games,
while Dynamic collections are those you can set filters or search texts. 

To create a new collection on EmulationStarion and enable them to be displayed on main screen/carousel:

On EmulationStation → Start → Game Collection Settings
1. Group unthemed custom collections (disabled)
2. Create new editable/dynamic collection
   1. Insert the name of the collection 
   2. See the list below for collection names that have a logo

## Currently supported franchises

There is a couple of logos for the following franchises:
- `Final Fantasy`
- `Mario`
- `Metroid`
- `Persona`
  - I like to create Persona collection as a dynamic collection and use the text `persona, megami tensei` as **Find Games** content, so the collection gathers all games with *Persona* and *Megami Tensei* in its titles (which includes Shin Megami Tensei as well).
- `Pokemon`
- `SaGa`
- `Zelda`

Miscellaneous Collections:
- `Grouvee Playing`

The names listed are case sensitive and with white spaces (like in `Final Fantasy`). If you use any variation like `MariO` or `final-fantasy` your collection will not display the logo.

<br>

# Supported Platforms

**Systems:** 
3DO,
Amiga,
Amiga CD32,
Amstrad CPC,
Atari 800,
Atari 2600,
Atari 5200,
Atari 7800,
Atari Lynx,
Atari ST,
Atomiswave,
Capcom PlaySystem 1,
Capcom PlaySystem 2,
Capcom PlaySystem 3,
Channel F,
Coleco Vision,
Commodore 16,
Commodore 64,
Commodore 128,
Commodore VIC-20,
Daphne,
Doom,
Dreamcast,
EasyRPG,
Famicom,
Famicom Disk System,
Final Burn Neo,
Game&Watch,
Gameboy & Hacks,
Gameboy Color & Hacks,
Gameboy Advance & Hacks,
Gamegear & Hacks,
Homebrew,
Intellivision,
Java,
Laserdisc,
Mame,
MasterSystem,
Megadrive / Genesis & Hacks,
Megaduck,
MS-DOS / PC,
MSX,
MSX2,
Naomi,
NEC Pc88,
NEC Pc98,
NeoGeo,
NeoGeo CD,
NeoGeo Pocket,
NeoGeo Pocket Color,
NES & Hacks,
Nintendo 64,
Nintendo DS,
Odissey²,
OpenBor,
PC Engine / TurboGrafx 16,
PC Engine CD / TurboGrafx CD,
PC Engine SuperGrafx,
PC-FX,
PICO-8,
PlayStation,
Ports,
Pokémini,
PSP,
PSP Minis,
Satellaview,
Saturn,
ScummVM,
SC-3000,
Sega 32x,
Sega CD / Mega CD,
SG-1000,
Sharp X1,
Sharp X68000,
Sinclair ZX81,
Sinclair ZX Spectrum,
Solarus,
Sufami,
Super Gameboy,
Super Famicom,
Super Nintendo & Hacks & MSU-1,
SuperVision,
Tic-80,
Uzebox,
Vectrex,
Videopac,
VirtualBoy,
Wolfenstein,
WonderSwan,
WonderSwan Color,
and Others.



**Collections:** 2 Players, 4 Players, Arcade, Arcade Vertical, Pistol Games, Screenshots, Custom Collections, Tools, Favorites, All Games, Never Played, Last Played, RetroAchievements, MPlayer.

<br>

# License

All [videogame and computer system logos](./assets/logos/) used are the property of their respective Developers/Producers/Distributors/Licensors.

Some logos were taken from [Dan Patrick's set](https://archive.org/details/console-logos-professionally-redrawn-plus-official-versions). (Thanks for the great work).

Some [fonts](./assets/fonts/) are licensed under Apache 2.0 and SIL Open Font License.

Some [icons](./assets/icons/) are licensed under Apache 2.0 or their respective license.

All the files, code and images not mentioned abore are licensed under the [MIT License](./LICENSE).

<br>

# Made With

![Inkscape](https://img.shields.io/badge/Inkscape-273445?style=for-the-badge&logo=Inkscape&logoColor=white)
![Visual Studio Code](https://img.shields.io/badge/Visual_Studio_Code-0d52bf?style=for-the-badge&logo=visual%20studio%20code&logoColor=white)
![And](https://img.shields.io/badge/And-f37329?style=for-the-badge&logoColor=white)
![Love](https://img.shields.io/badge/Love-de3e80?style=for-the-badge&logoColor=white)
