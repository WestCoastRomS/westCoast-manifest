
# WestCoastRomS #
[<center><img src="https://avatars1.githubusercontent.com/u/55059493?s=460&v=4/.png" height="90%" width="90%;"/></center>](https://github.com/WestCoastRomS)

## Getting WCR's source ## 
repo init -u https://github.com/WestCoastRomS/WCRoms-final.git-b wcroms-9.0

to sync the repo type=       

repo sync --force-sync -j$( nproc --all )

## Setting up your build environment and syncing the source ##
To set up your build environment and sync WestCoastRomS, please follow this guide: [Link](https://raw.githubusercontent.com/nathanchance/Android-Tools/master/Guides/Building_AOSP.txt)

## Submitting Patches ##
WestCoastRomS is an open source project and welcomes new contributors. I am not a senior DEV by any means, so feel free to make additions and submit a pull request. If its awesome ill add it! :)


As this project is new stuff will be added as I go. Thanks for choosing WestCoastRomS.


# Android Make Build System

This is the Makefile-based portion of the Android Build System.

For documentation on how to run a build, see [Usage.txt](Usage.txt)

For a list of behavioral changes useful for Android.mk writers see
[Changes.md](Changes.md)

For an outdated reference on Android.mk files, see
[build-system.html](/core/build-system.html). Our Android.mk files look similar,
but are entirely different from the Android.mk files used by the NDK build
system. When searching for documentation elsewhere, ensure that it is for the
platform build system -- most are not.

This Makefile-based system is in the process of being replaced with [Soong], a
new build system written in Go. During the transition, all of these makefiles
are read by [Kati], and generate a ninja file instead of being executed
directly. That's combined with a ninja file read by Soong so that the build
graph of the two systems can be combined and run as one.

[Kati]: https://github.com/google/kati
[Soong]: https://android.googlesource.com/platform/build/soong/+/master

