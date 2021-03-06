# HFPS-Chromium
Chromium Module for Highly Flexible Profiling System

## Introduction

Chromium Module for Highly Flexible Profiling System (`HFPS-Chromium`) is an implementation of [*a*STEAM Project](https://asteam.korea.ac.kr)'s Highly Flexible Profiling System (HFPS) compatible with [Chromium](https://http://www.chromium.org/Home) which is the open-source browser project of Google. This module extracts timing and frame data from the browser and writes extracted data to a proc file.

## Requirements and Dependencies

* *Chromium (65.0.3317.0)*: Follow the [instructions of the docs](https://chromium.googlesource.com/chromium/src/+/master/docs/android_build_instructions.md)
* [*ADB shell*](http://adbshell.com/)

## Build/Install Instructions
1. cd chromium/src
2. patch -p0 < mobed_chromium.patch
3. gn gen --args='target_os'="android" out/Default
4. ninja -C out/Default chrome_modern_public_apk
5. adb install chromium/src/out/Default/apks/ChromeModernPublic.apk
