# HFPS-Chromium
Chromium Module for Highly Flexible Profiling System (HFPS)

## Introduction

Chromium Module for Highly Flexible Profiling System (`HFPS-Chromium`) is an implementation of *a*STEAM Project <https://asteam.korea.ac.kr>'s Highly Flexible Profiling System (HFPS) compatible with Chromium which is one of the open-source browser project <https://http://www.chromium.org/Home> of Google. This module extracts timing and frame data from the browser, and writes extracted data to a proc file.

## Requirements and Dependencies

* *Chromium*: Follow the [instructions of the docs](https://chromium.googlesource.com/chromium/src/+/master/docs/android_build_instructions.md)
* [*ADB shell*](http://adbshell.com/)

## Instructions

* Build/Install Instructions of `HFPS-Chromium`
** cd chromium/src
** patch -p0 < mobed_chromium.patch
** gn gen --args='target_os'="android" out/Default
** ninja -C out/Default chrome_modern_public_apk
** adb install chromium/src/out/Default/apks/ChromeModernPublic.apk
