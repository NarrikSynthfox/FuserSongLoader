# Fuser Song Loader

## Introduction

A dll used to load custom songs in Fuser.

### How it works

This song loader works as a standalone DLL (`winhttp.dll`). It get loaded by Fuser when it starts up.

### How to use it

* Download the latest files from [the releases page](https://github.com/NarrikSynthfox/FuserSongLoader/releases) 
* Extract everything to the same directory as `Fuser-Win64-Shipping.exe`. (Should be somewhere like C:/Program Files (x86)/Steam/steamapps/common/Fuser/Fuser/Binaries/Win64)
* Create a `custom_songs` folder in the content pak directory (Should be somewhere like C:/Program Files (x86)/Steam/steamapps/common/Fuser/Fuser/Content/Paks/)
* Add any custom song .pak + .sig files to that directory. (These can be created with [Fuser Custom Song Creator](https://github.com/NarrikSynthfox/FuserCustomSongCreator))

⚠️ After adding or removing custom songs, make sure to delete your `customSongsUnlocked_P.pak` and `customSongsUnlocked_P.sig` files in `.../Fuser/Fuser/Content/Paks` (the folder above `custom_songs`). The file will regenerate with your new roster on game load.

## Building

```bash
git clone https://github.com/NarrikSynthfox/FuserSongLoader.git
cd FuserSongLoader
git submodule update --init --recursive
./build.bat
```
`FuserSongLoader.sln` should be generated under the `FuserSongLoader/build` folder.

1. Building the `FuserModDoorstop` `Visual Studio` project will output a `winhttp.dll`, which should be placed next to `Fuser-Win64-Shipping.exe`
