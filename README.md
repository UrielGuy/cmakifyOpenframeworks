# cmakifyOpenframeworks
A CMake file allowing you to integrate openframeworks into a CMake project

## Description

Adding this file to your CMake tree allows you to add `openframeworks` as a link library, and link it to
your own projects. No other action required. Additionally it defines the `ofxGui` and `ofxAssimpModelLoader`
addons, so you can see how to add more of them if you need them. 

## How does it do it? 

When creating a CMake project, this will download the latest release of OpenFrameworks for your platform,
patch it a bit, compile it, and define it as a library availbale for linking. This script will: 

* Download and extract everything to a cached directory (so openframeworks is only compiled once for all projects)
* Get the latest version (0.11.2) for windows, macos and armv6, and the latest nightly for Arm AARCH64
* Will patch the compilation and dependencies so they can support compilation into a Shared object (enable -fPIC for everything).
* Will rebuild openFrameworks if the CMake file ever updates

## Requirements

On all platforms: 
* git
* cmake

on windows: 

* Visual studio 2017 and up

on all others: 

* To have run the openFrameworks install_dependencies.sh script successfully





