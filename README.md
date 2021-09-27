<div align="center">
    <h1><img src="icon.png" height="22px"> Pokémon RBY DX</h1>
    <h4><b>🎮 GBC-enhanced ROM hacks of Pokémon Red, Blue and Yellow</b></h4>
    <h4>
        <a href="#goals">Goals</a>
        •
        <a href="#versions">Versions</a>
        •
        <a href="#development-guidelines">Development guidelines</a>
        •
        <a href="#wiki">Wiki</a>
        •
        <a href="#contributors">Contributors</a>
        •
        <a href="#disclaimer">Disclaimer</a>
        •
        <a href="#licence">Licence</a>
    </h4>
    <h3>
        <a href="https://www.github.com/andiemmadavies">
            <img src="https://img.shields.io/badge/maintainer-%40andiemmadavies-yellow">
        </a>
        <a href="https://www.github.com/AmateurPanda/pokemon-rby-dx/commit/e1661bd0de07129225c6af9b5e9706db87920902">
            <img src="https://img.shields.io/badge/initial%20commit-5th%20september%202019-brightgreen">
        </a>
        <a href="https://www.github.com/AmateurPanda92/pokemon-rby-dx/commits/main">
            <img src="https://img.shields.io/github/last-commit/AmateurPanda92/pokemon-rby-dx?color=blue&label=last%20updated">
        </a>
        <a href="https://www.github.com/AmateurPanda92/pokemon-rby-dx/releases/latest">
            <img src="https://img.shields.io/github/v/release/AmateurPanda92/pokemon-rby-dx?color=blueviolet&label=latest%20release">
        </a>
        <a href="#licence">
            <img src="https://img.shields.io/badge/licence-%C2%A9%20%2B%20MIT-crimson">
        </a>
    </h3>
</div>

---

<div align="center">
   <h3><b>Sister project:</b> <a href="https://www.github.com/AmateurPanda92/understanding-pokemon-red-english-translation">Pokémon Red – Detailed Disassembly Documentation 📚</a></h3>
   <p>I recently stumbled upon <a href="https://www.github.com/pokemium">@pokemium</a>’s superb, albeit WIP, resource <a href="https://www.github.com/pokemium/understanding-pokemon-red">詳解ポケモン赤 / “Understanding Pokémon Red”</a> and I’ve started work on translating it to English (the repo linked above). I’ll work on continuing this translation effort as I go through this project, as in doing so, it’ll become more useful as source code documentation to anyone working on RBY DX, and I may even be able to contribute back some original research of my own to help fill-in any gaps in the original repo’s information.</p>
</div>

---

_(**tl;dr** – if you just want to try the ROMs out, the [releases](https://github.com/AmateurPanda92/pokemon-rby-dx/releases) tab contains pre-compiled binaries of each version which you can download as is and try-out in any decent GBC emulator.)_

This is a work-in-progress fan-made [ROM hack](https://en.wikipedia.org/wiki/ROM_hacking) of the [first-generation](https://en.wikipedia.org/wiki/Pok%C3%A9mon_(video_game_series)#First_generation_(1996%E2%80%931999)) [Pokémon](https://en.wikipedia.org/wiki/Pok%C3%A9mon) [games](https://en.wikipedia.org/wiki/Pokémon_(video_game_series)), which were originally developed for the [Nintendo](https://en.wikipedia.org/wiki/Nintendo) [Game Boy (DMG)](https://en.wikipedia.org/wiki/Game_Boy) and are planned here to be enhanced specifically for the Nintendo [Game Boy Color (GBC)](https://en.wikipedia.org/wiki/Game_Boy_Color). All backwards compatibility with the original Game Boy will be removed so that it doesn’t hold-back what the games might be capable of imagining they were originally intended to be GBC-exclusive titles.

The inspiration for this project comes from the likes of the excellent fan-made DX/“deluxe” ROM hacks such as [_Super Mario Land DX_](http://www.romhacking.net/hacks/4477) and [_Super Mario Land 2 DX_](http://www.romhacking.net/hacks/3784), which in turn were likely inspired by official upgraded titles back in the day like [_Tetris DX_](https://en.wikipedia.org/wiki/Tetris_(Game_Boy)#Tetris_DX) and [_The Legend of Zelda: Link’s Awakening DX_](https://en.wikipedia.org/wiki/The_Legend_of_Zelda:_Link%27s_Awakening). These offer full [15-bit colour](https://en.wikipedia.org/wiki/Game_Boy_Color#Summary), usually fixes for well-known bugs in the original DMG counterparts and often additional features, such as new playable characters, new gameplay modes, improved sprite graphics, extra levels, peripheral integration, game mechanics that mandate the use of colour, and so on.

In essence, I want to make this game as polished as might have been possible back in the day if the limitations of the original weren’t as strict, i.e. if they didn’t have to worry about manufacturing costs on a commercial scale, didn’t have to worry about delivering a product in a certain timeframe, could use the maximum number of [ROM banks](https://en.wikipedia.org/wiki/Bank_switching), could exploit the [extra processing power and RAM](https://en.wikipedia.org/wiki/Game_Boy_Color#Specifications) of the GBC and weren’t limited to the monochrome DMG colour palette. I do still want the game to _feel_ like the 1<sup>st</sup>-gen games though, so I will have to draw a line somewhere regarding upgrades, for instance, I doubt I’ll add features like the [in-battle experience points progress bar](https://bulbapedia.bulbagarden.net/wiki/Pok%C3%A9mon_Gold_and_Silver_Versions#Graphics), otherwise this might detract from the game feeling authentic.

This project is based-on the superb split-assemblies of [Red, Blue](https://www.github.com/pret/pokered) and [Yellow](https://www.github.com/pret/pokeyellow) created by the [pret](https://www.github.com/pret) collective, and wouldn’t have been possible without their contributions to the scene, so a **huge** thanks to all of them! The list of contributors to each of these repositories can be found here:

* https://www.github.com/pret/pokered/graphs/contributors
* https://www.github.com/pret/pokeyellow/graphs/contributors

As it stands, this project is very much a work-in-progress – so much so that there haven’t yet been any changes to the source code, so building the repository will result in two binaries that are bit-perfect copies of known-good dumps of the official releases of Blue and Red (see below). As such, my first goal with this project will be to have a play with the shiny new [GitHub Actions](https://www.github.com/features/actions) platform and get it building the source automatically. As of [v0](https://github.com/AmateurPanda92/pokemon-rby-dx/releases/tag/v0) of this project, the ROMs generated will be the following named entries from the [Cowering GoodTools](http://emulation.gametechwiki.com/index.php/GoodTools) database, and associated message-digest hash, where the _“(UE)”_, _“[S]”_ and _“[!]”_ [codes](http://emulation.gametechwiki.com/index.php/GoodTools#Good_codes) indicate that the ROM binary is for the USA and Europe regions, has special [Super Game Boy](https://en.wikipedia.org/wiki/Super_Game_Boy) integration and is an exact copy of the original game without modifications respectively:

* _“Pokemon Red (UE) [S][!].gb”_ (MD5: `3d45c1ee9abd5738df46d2bdda8b57dc`)
* _“Pokemon Blue (UE) [S][!].gb”_ (MD5: `50927e843568814f7ed45ec4f944bd8b`)

I will always be keeping this README up-to-date with the state of the codebase, so this will remain a reliable single point-of-truth for the project’s status. Note that this project is primarily a learning tool for me to teach myself GB(C) development and gain more experience with coding in assembly. That being said, I more than welcome contributors to come and get involved, so please do get in-touch (probably via [Twitter](https://www.twitter.com/andiemmadavies) is best) if you’re interested in helping-out!

## Table of contents

* [Goals](#goals)
  * [Development](#development)
  * [Compatibility](#compatibility)
  * [Fixes](#fixes)
  * [Graphics](#graphics)
  * [UI/UX](#uiux)
  * [Events](#events)
  * [Extras](#extras)
* [Versions](#versions)
  * [Numbering](#numbering)
  * [Releases](#releases)
  * [Roadmap](#roadmap)
* [Development guidelines](#development-guidelines)
  * [Building](#building)
    * [First-time setup](#first-time-setup)
      * [Windows 10](#windows-10)
      * [Windows 8.1 and below](#windows-81-and-below)
      * [macOS](#macos)
      * [Linux](#linux)
        * [Debian or Ubuntu](#debian-or-ubuntu)
        * [OpenSUSE](#opensuse)
        * [Arch Linux](#arch-linux)
        * [Termux](#termux)
    * [To build](#to-build)
  * [Running](#running)
* [Wiki](#wiki)
  * [Assets](#assets)
  * [Contributions](#contributions)
  * [Research](#research)
  * [Resources](#resources)
  * [Specifications](#specifications)
* [Contributors](#contributors)
  * [Project staff](#project-staff)
  * [pret repos’ contributors](#pret-repos-contributors)
* [Disclaimer](#disclaimer)
* [Licence](#licence)

## Goals

The following is a fairly comprehensive, but not necessarily exhaustive, list of what I’m striving to achieve with this project, sorted into rough categories…

### Development

* I’m looking to develop this hack using **modern development tools and methodologies**, including (but not limited to): [open source](https://www.opensource.com/resources/what-open-source), task tracking and management, community engagement, full version control, [SemVer](https://semver.org/) version numbering scheme, [feature branch workflow](https://www.atlassian.com/git/tutorials/comparing-workflows/feature-branch-workflow), peer code review, collaborative coding tools, automated build process, separate debug and release build configurations, automated testing (if practical), [CI/CD](https://en.wikipedia.org/wiki/CI/CD), develop new tooling, crowd-sourced pre-release testing, ongoing public documentation efforts, etc.
* I plan for changes to be **implemented roughly in the order players will first experience them in-game**, so that demo and preview builds are already close to 100% polished up to a certain point of in-game progress, i.e. I’ll start with the copyrights screen, then the Game Freak logo, opening cutscene, title screen, and so on.
* One of the earliest changes I’d like to make is to **add a version number indicator to the title screen**, so that each build in the wild is clearly distinguishable by just loading the game. I’d also like to get the necessary scaffolding set-up for this version number to be automatically set at build time, so that releases automatically show their correct version number in-game.
* As and when they become necessary, I’ll add **bespoke in-game debugging tools**, which will only be available when built via the debug build config.

### Compatibility

* The key change here is that I will **immediately ditch DMG backwards compatibility**, so that the hack can exploit all the GBC-exclusive hardware goodies.
* **Real hardware support**, with the hope of eventually getting some **real cartridges manufactured** (maybe even with new box designs and the like too).
* Maintain (and expand on) **full [Game Link Cable](https://en.wikipedia.org/wiki/Game_Link_Cable) compatibility**, including:
  * Support for using the **[Game Boy Printer](https://en.wikipedia.org/wiki/Game_Boy_Printer)**:
    * Print **[stickers](https://bulbapedia.bulbagarden.net/wiki/Game_Boy_Printer#Pok.C3.A9dex_stickers) of every Pokémon** in the Pokédex, featuring their updated sprite graphics.
    * Print a custom **completed-Pokédex [diploma](https://bulbapedia.bulbagarden.net/wiki/Game_Boy_Printer#Diploma)**, featuring special graphics for the completing it on the DX editions.
    * Print a list of **Pokémon stored in a [Storage System](https://bulbapedia.bulbagarden.net/wiki/Game_Boy_Printer#Pok.C3.A9mon_Storage_System) box**, as in the originals.
    * Print [**party Pokémon “photos”**](https://bulbapedia.bulbagarden.net/wiki/Game_Boy_Printer#Party_Pok.C3.A9mon) when visiting the chairman of the Pokémon Fan Club in Vermillion City.
    * In addition, I’d like to be able to **add GB Printer support to the Red and Blue editions**, as only Yellow featured printing functionality in the original releases.
  * **Full trade and colosseum compatibility** with both 1<sup>st</sup>- and 2<sup>nd</sup>-gen (via the [Time Capsule](https://bulbapedia.bulbagarden.net/wiki/Time_Capsule)) mainstream Pokémon games (English-language versions only).
  * I probably **won’t keep support for interacting w/ Pokémon Stadium**, as I have to draw the line somewhere. Plus, this would be an absolute nightmare to debug, if not impossible for anyone without an N64 development kit! You never know, it may JustWork™ if I’m lucky and don’t make too many alterations to memory locations for existing Pokémon data.
  * Ultimately, I don’t want this game to be considered a gimmick. I’d like it to be able to interact with the official games, as if it were an official release itself.
  * (Maybe even some currently unimagined uses that could be explored in future too…)
* Brand **new custom [Super Game Boy](https://en.wikipedia.org/wiki/Super_Game_Boy) borders** for each of the three editions.

### Fixes

* **Fix as many [well-known bugs](https://bulbapedia.bulbagarden.net/wiki/List_of_glitches_in_Generation_I) and [oversights](https://bulbapedia.bulbagarden.net/wiki/Generation_I#Issues_and_bugs) as possible** from the originals, especially those that cause game instability or make it impossible to progress without starting a new game.
* **Fix any bad Japanese to English translations**.
* I will also make the necessary changes to **stop it being possible to perform a variety of glitches** like the [Mew glitch](https://bulbapedia.bulbagarden.net/wiki/Mew_glitch), mostly for stability and completeness, so the game feels polished, plus they likely won’t work the same once memory locations start to shift anyway.
* I aim to **fix newly-introduced bugs as a priority** before starting work on new features, otherwise everything will quickly become an unplayable mess!

### Graphics

* The obvious one: **full colour everywhere**!
* **Background graphics** (or at least colours) for battles, cutscenes, etc.
* All **new Pokémon sprites**, both for in-battle (front and back, designed to more closely resemble the anime-inspired art style that became the standard after Red and Blue were released) and in the party menu.
* Maybe **double the resolution of the rear-facing battle sprites**?
* **Fly and Surf graphics that show the actual Pokémon** that performed the move in the overworld, rather than just the generic Seel and Pidgey graphics.
* **HP bar which gradually changes colour** from green to red, like in Yellow but even more gradually.
* **Tweaked trainer sprites**, to be more in-line with the anime aesthetic that the new Pokémon sprites will be designed to adhere to.
* **Antialiased text** and other UI elements like **menu and textbox borders** (might be too ambitious). Maybe support for [variable-width fonts](https://www.youtube.com/watch?v=xm7Iv4aKFGk)?

### Audio

* Sound will largely remain unchanged. It should, however, be possible to **improve the sound quality of Pikachu’s cry and voice clips** in Yellow: can double the sample rate, since the game can now use the GBC-exclusive double CPU clock speed and can utilise more ROM banks to store higher-resolution samples. Might also be able to squeeze some less harsh downsampling out of the effective 2-bit (variable amplitude) bit depth by playing around with different dithering methods and input levels when re-encoding the sound data. This is all assuming I can get hold of the original, uncompressed voice samples from somewhere ([Retro Game Mechanics Explained](https://www.youtube.com/watch?v=fooSxCuWvZ4) managed to find them somewhere).
* There appears to exist at least one **unused hidden track** in the original ROM data, which could potentially be used for a new feature addition to the game.
* Could maybe port the **2<sup>nd</sup>-gen games’ audio engine** over, in order to be able to use the richer instrument sounds (possibly with a user option to select which version they’d prefer to hear).

### UI/UX

* Add **UI niceties** that were added in future generations, such as:
  * **Select button quick items** (e.g. for bicycle).
  * **Press A to interact with objects** like cuttable trees, boulders, etc.
  * **Signposts** that appear onscreen **when you enter a new area**.
  * [**Run by holding ‘B’**](https://www.github.com/pret/pokered/wiki/Running-Shoes), similar to the running shoes introduced in gen-3.
  * [**Turning to face enemy trainers when seen**](https://www.github.com/pret/pokered/wiki/Turn-to-face-enemy-trainers-when-seen-by-them), introduced in the non-remake 3<sup>rd</sup>-gen games.
  * **Turbo mode** that makes use of the GBC’s double clock speed compared to the DMG, giving players the option to speed-up gameplay like they’d be able to if using an emulator. It might not be possible to double the clock speed at run time, so one way this might be possible is to always run the game at double clock speed and limit the speed at which graphics and audio are updated.
* **UX behaviour tweaks** and other **quality-of-life improvements** to address minor friction points that negatively affect the player’s enjoyment, for example:
  * Allowing the player to **cancel playing the bicycle music** by pressing ‘B’ when riding the bike to revert to the music attributed to the area they are in, similar to the effect moving into a new area while still on the bike would have.
  * Removing or [**reducing the artificial save delay**](https://www.github.com/pret/pokered/wiki/Remove-Artificial-Save-Delay).

### Events

* Plan some cool new in-game event that makes it **possible to catch a genuine Mew** without the Mew glitch (as I plan to [patch that glitch out](#Fixes)). Maybe Mew actually _is_ [under the truck](https://www.kotaku.com.au/2017/02/that-time-some-players-thought-mew-was-under-a-truck-inpokmon) after all!?
* An in-game event that makes it possible to catch a **genuine surfing Pikachu** without requiring the use of Pokémon Stadium (as I plan to [remove support for it](#Compatibility)) and a Transfer Pak; maybe make it a single field encounter like with the other legendaries?
* Restore the long-lost **final battle with Oak**, and other [speculated cut content/features](https://bulbapedia.bulbagarden.net/wiki/Professor_Oak#Unused_teams).

### Extras

* **Cameos and Easter eggs**? Maybe some anime references? _“Ash was here”_ for instance? Staff and contributor battles?
* I’ve often thought about developing **a version of the gen-I games which closely matches the anime**, so maybe this will serve as a good base for that when this project is largely finished? Who knows!
* After beating the game, maybe **provide limited access to Johto via the SS Aqua** like at the end of Gold/Silver/Crystal, to tie the generations together? Maybe [v2](#Roadmap) could let you play _all_ of Johto with similar enhancements? Also Gold and Silver still had DMC compatibility, so the gen-II games didn’t make use of all colour that was available to it, nor did it use the extra RAM and processing power. Crystal made use of some of the extra RAM or processing power I believe, in order to do the animated in-battle Pokémon sprites but I don’t think it added any additional colour usage (unless I can find evidence to the contrary), so Johto could equally be enhanced colour and graphics wise.
* [v3](#Roadmap) could include **support for trading and battling with gen-III**, possibly by developing some custom hardware that bridges the different link cable versions, which would allow for genuine trading between generations so that genuine gen-I/II Pokémon could be traded forward to official gen-III games.

## Versions

### Numbering

The versioning scheme for this project is loosely based around [Semantic Versioning](https://semver.org/), where the version number is split into up to five parts:

1. _**Major** number_ – this is incremented when the codebase has significantly changed since its last major revision, i.e. for the final version, then for each major new release-worthy set of changes, such as new regions to explore, new game mechanics, etc. Incrementing this number resets the minor, patch and pre-release parts to zero/unspecified.
2. _**Minor** number (optional, prefixed by a full stop, must be present if patch number is specified)_ – this is incremented every time there has been a new feature added or the codebase has undergone a large refactor. Incrementing this number resets the patch and pre-release parts to zero/unspecified.
3. _**Patch** number (optional, prefixed by a full stop, must be present if pre-release label is specified)_ – this is incremented whenever a bug gets fixed or a small feature/refactor has been implemented. Incrementing this number resets the pre-release parts to zero/unspecified.
4. _**Pre-release label** string (optional, prefixed by a hyphen, must be present if pre-release revision is specified)_ – this is set whenever a version of the codebase is made available for others to test, and can be one of three values (in order of precedence): _“alpha”_ (early public preview), _“beta”_ (feature freeze for bug-bashing) and _“rc”_ (release candidate, i.e. the version of the code to be released unless any bugs emerge in the meantime). Promoting this label to the next value resets the pre-release revision to zero/unspecified.
5. _**Pre-release revision** number (optional, prefixed by a full stop)_ – this is set whenever a pre-release stage needs updates applying to it and is incremented for each time this needs to happen.

### Releases

_(There have been no releases yet; watch this space!)_

### Roadmap

I plan to keep chipping-away at this project for years to come, hence some of the wildly ambitious future major version update ideas below! This is my current list of aspirations for the project, along with rough associated version numbers:

* **v0** - the original, unmodified game (used primarily for testing CI/CD with GitHub Actions).
* **v0.0.x** - initial set of codebase-tidying refactors.
* **v0.1** - runs in GBC-exclusive mode.
* **v0.1.1** - proof-of-concept with some change that proves that more than DMG colours are available to the game.
* **v0.2** - first proper user-visible change (which will probably be changes to the copyright screen).
* **v0.x** - incremental feature upgrades (in the order outlined previously).
* **v0.y-alpha** - initial publicised demo (with areas restricted using feature flags for stability). Maybe cut-off once you’re allowed to go into the grass properly after Oak’s already dragged you inside the lab and you’ve battled Blue.
* **v0.z-beta** - the vast majority of, if not all, new features have been developed, to the point where the game can be completed and there’s always something new visible, but there will likely be lots of bugs to be squashed. It’s at this point we’ll be appealing for beta testers to help get the game ready for its initial [GA](https://en.wikipedia.org/wiki/Software_release_life_cycle#General_availability_(GA)) release.
* **v1-rc** - release candidate for the first full release of the game. If no bugs are found between the publishing of this version and the release date, then this will be the version of the code that gets promoted to full release as v1.
* **v1** - first completed release of the game, to be published with an accompanying [github.io](https://pages.github.com/) website and advertising campaign of sorts.
* **v1.0.x** - post-release bug fixes to the original feature set of v1. No new features.
* **v1.x** - new feature development approaching v2.
* **v2** - the next major iteration of the game; practically a standalone new hack. This could be something like adding the Johto region to the game.
* **v3** - maybe something super-ambitious and technically challenging that extends beyond just the software, such as to support trading with the 3<sup>rd</sup> generation games, something that was never officially supported?
* **vX** - who knows!!

## Development guidelines

### Building

#### First-time setup

##### Windows 10

_(Note that you can also use the Cygwin-based setup from the [Windows 8.1 and below](#windows-81-and-below) section if you like, it’s mostly a matter of personal preference.)_

1. Open an elevated (“as administrator”) PowerShell instance and run the following command to enable Windows Subsystem for Linux (aka “WSL”):
   * `dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart`
2. If you’re running Windows 10 version 2004 (build 19041) or later, you can benefit from the speed improvements of version 2 of WSL – if not, skip to _step 6_. To do so, install WSL 2 by running the following in the elevated PowerShell instance:
   * `dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart`
3. Reboot to complete the upgrade to WSL 2.
4. When rebooted, download and install the following Linux kernel update package MSI:
   * https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi
5. Run the following in PowerShell to set WSL 2 as the default version:
   * `wsl --set-default-version 2`
6. Install your Linux distribution of choice from the Microsoft Store application.
7. Reboot your machine before continuing to allow WSL to finish installing itself.
8. Once installed, open the Linux distro and follow the on-screen instructions to perform initial OS setup and create a user for yourself.
9. Follow the [Linux](#linux) first-time setup instructions for the distro you chose.

##### Windows 8.1 and below

1. Download and run the [Cygwin installer](https://www.cygwin.com/install.html).
2. Progress through the installation wizard until you reach the _“Select Packages”_ section.
3. Select the latest version of the following packages to install:
   * `gcc-core`
   * `make`
4. Proceed with the installation.
5. Download the latest [Rednex Game Boy Development System](https://www.github.com/rednex/rgbds) (RGBDS) [release](https://www.github.com/rednex/rgbds/releases) for Windows and extract it.
6. Place the extracted files into the following directory, where `<Cygwin>` is the path to where you installed Cygwin:
   * `<Cygwin>\usr\local\bin`

##### macOS

1. Open a Terminal instance and run the following command to install Homebrew:
   * `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"`
2. Install RGBDS by running the following:
   * `brew install rgbds`

##### Linux

###### Debian or Ubuntu

1. Run the following to install all the necessary components:
   * `sudo apt-get install make git gcc pkg-config flex bison libpng-dev`
2. Clone the RGBDS repo on the branch for v0.4.0 with the following command:
   * `git clone -b v0.4.0 --depth=1 https://github.com/rednex/rgbds`
3. Install RGBDS by running the following:
   * `sudo make -C rgbds install`

###### OpenSUSE

1. Run the following to install all the necessary components:
   * `sudo zypper install make gcc git zypper install pkg-config flex bison libpng16-devel`
2. Clone the RGBDS repo on the branch for v0.4.0 with the following command:
   * `git clone -b v0.4.0 --depth=1 https://github.com/rednex/rgbds`
3. Install RGBDS by running the following:
   * `sudo make -C rgbds install`

###### Arch Linux

1. Run the following to install all the necessary components:
   * `sudo pacman -S make gcc git pkg-config flex bison libpng`
2. Clone the RGBDS repo on the branch for v0.4.0 with the following command:
   * `git clone -b v0.4.0 --depth=1 https://github.com/rednex/rgbds`
3. Install RGBDS by running the following:
   * `sudo make -C rgbds install`

###### Termux

Run the following to install all the necessary components:

* `sudo apt install make clang git sed rgbds`

#### To build

1. Launch an instance of your platform’s terminal application.
2. Set the working directory to the root of the repository, replacing `<path-to-repo>` with the path to said repository root:
   * `cd <path-to-repo>`
3. Issue the following commands to generate the desired output binaries to the repo’s root directory (note that this will take a while on first build, but builds are incremental, so only changed source files will be recompiled when run again):
   * `make red` – generates a **Red-version** binary with a filename of _“pokered.gbc”_.
   * `make blue` – generates a **Blue-version** binary with a filename of _“pokeblue.gbc”_.
   * `make` – generates binaries for **both** versions with filenames of _“pokered.gbc”_ and _“pokeblue.gbc”_ respectively.

### Running

As far as I know, [mGBA](https://www.mgba.io/) is the most accurate GBx emulator for PC that is still in active development, so this is the one I’m going to be using as a reference emulator and what I recommend contributors use as well. Download the 64-bit Windows archive of the [latest release](https://www.github.com/mgba-emu/mgba/releases/latest) (e.g. _“mGBA-X.Y.Z-win32.7z”_, where _‘X’_, _‘Y’_ and _‘Z’_ are the three parts of the version number), extract it using [7-Zip](https://www.7-zip.org/), run mGBA and open one of the game binaries that was built from the steps in the previous section in order to test the game and any changes made.

If you’re not a PC user, mGBA has builds for macOS and Ubuntu too, so that should cover most bases if you develop on a different platform. There are tonnes of good open-source emulators out there though, so do some digging and I’m sure you’ll find one that does the job…

## Wiki

There is now a [repository wiki](https://www.github.com/AmateurPanda92/pokemon-rby-dx/wiki) that contains more detailed information about project specifics than on this README. We’ll add to it as and when there are new aspects of the project that need documenting, and it’ll eventually become a one-stop shop for information pertaining to the project. It might even be possible in future for any original research to be shared back to the wider ROM hacking community too.

At the time of writing (5<sup>th</sup> January 2021), these are the existing sections and sub-pages on the wiki…

### [Assets](https://www.github.com/AmateurPanda92/pokemon-rby-dx/wiki/Assets)

Any newly-designed graphical assets are documented here for quick reference, as well as a evision history for each:

* [**Pokémon sprites**](https://www.github.com/AmateurPanda92/pokemon-rby-dx/wiki/Pokémon-Sprites)

### [Contributions](https://www.github.com/AmateurPanda92/pokemon-rby-dx/wiki/Contributions)

If you’d like to contribute towards this project, please follow these guidelines to ensure we are moving in a unified direction with consistent code and assets:

* [**Artwork**](https://www.github.com/AmateurPanda92/pokemon-rby-dx/wiki/Artwork)

### [Research](https://www.github.com/AmateurPanda92/pokemon-rby-dx/wiki/Research)

The outcome of any research work is recorded here for future reference. If any of the research here is new, we can contribute it back to the community in due course as well:

* [**Palette limitations**](https://www.github.com/AmateurPanda92/pokemon-rby-dx/wiki/Palette-Limitations)

### [Resources](https://www.github.com/AmateurPanda92/pokemon-rby-dx/wiki/Resources)

A variety of useful resources are listed here, which could be anything from external documentation to software tools:

* [**General**](https://www.github.com/AmateurPanda92/pokemon-rby-dx/wiki/Resources#general)
* [**Documentation**](https://www.github.com/AmateurPanda92/pokemon-rby-dx/wiki/Resources#documentation)
* [**Software tools**](https://www.github.com/AmateurPanda92/pokemon-rby-dx/wiki/Resources#software-tools)

### [Specifications](https://www.github.com/AmateurPanda92/pokemon-rby-dx/wiki/Specifications)

A technical reference for any existing hardware or software specifications relevant to the game, as well as for documenting any new data structures, algorithms, etc.:

* [**GBC hardware**](https://www.github.com/AmateurPanda92/pokemon-rby-dx/wiki/GBC-Hardware)
* [**Pokémon graphics**](https://www.github.com/AmateurPanda92/pokemon-rby-dx/wiki/Pokémon-Graphics)

## Contributors

### Project staff

<table>
    <tr>
        <td width="200px">
            <a href="https://www.github.com/andiemmadavies">
                <img src="andi.png" width="200px">
            </a>
        </td>
        <td>
            <h4>Andi Emma Davies (<a href="https://www.github.com/andiemmadavies">@andiemmadavies</a>)</h4>
            <h5>Project lead and lead developer</h5>
            <p>A full-time software engineer by trade and lover of all things retro: I (Andi) have been looking for an excuse for a long time to do some kind of game development, so I devised this open project to coincide with my plans to start a retro gaming YouTube channel, with the hope that this can eventually become a community effort, rather than just a two-person venture.</p>
        </td>
    </tr>
    <tr>
        <td width="200px">
            <a href="https://www.github.com/JackalOfTime">
               <img src="farley.png" width="200px">
            </a>
        </td>
        <td>
            <h4>Farley Lapenna (<a href="https://www.github.com/JackalOfTime">@JackalOfTime</a>)</h4>
            <h5>Lead artist</h5>
            <p>Fresh out of a game design degree, Farley is looking to cut her teeth on some real-world game art projects, so I invited her to join me on this fun little fan hack, to add some open-source goodness to her growing portfolio.</p>
        </td>
    </tr>
</table>

### [pret](https://www.github.com/pret) repos’ contributors

And, of course, a huge thanks to everyone who maintains and contributes to the [_“pokered”_](https://www.github.com/pret/pokered/graphs/contributors) disassembly base repository this repo was forked from (and its sister project [_“pokeyellow”_](https://www.github.com/pret/pokeyellow/graphs/contributors)), without whom this project wouldn’t exist!

## Disclaimer

In order to download and run this game, you **must** have purchased a legal copy of _Pokémon Red Version_, _Pokémon Blue Version_ and/or _Pokémon Yellow Version: Special Pikachu Edition_ (depending on which version(s) you intend to run) before doing so. We do not endorse or condone piracy; it is your responsibility to ensure you own a legal copy of the original game and we accept no liability for any litigation that may occur in the event that you choose to use this reverse-engineered code for reasons of piracy.

## Licence

All code, assets and design elements (including but not limited to graphics/artwork, audio data / music, story and characters) that were present in the original unedited ROMs and their associated disassemblies remain the intellectual property of their original copyright holders:

* **Copyright © Nintendo 1995–2021**
* **Copyright © Creatures Inc. 1995–2021**
* **Copyright © GAME FREAK Inc. 1995–2021**

Portions of this code and assets (including but not limited to graphics/artwork and audio data / music) that has been altered from the original version of the game, are released until an [MIT licence](LICENCE):

* **Copyright © Andi Emma Davies 2020–21**
* **Copyright © Farley Lapenna 2020–21**
