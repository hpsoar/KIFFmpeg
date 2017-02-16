# 说明
FFmpeg 编译脚本来源于：[https://github.com/kewlbear/FFmpeg-iOS-build-script](https://github.com/kewlbear/FFmpeg-iOS-build-script)， 感谢原作者。

# 安装
pod 'KIFFmpeg'

# FFmpeg iOS build script

[![Build Status](https://travis-ci.org/kewlbear/FFmpeg-iOS-build-script.svg?branch=master)](https://travis-ci.org/kewlbear/FFmpeg-iOS-build-script)
[![Flattr this git repo](http://api.flattr.com/button/flattr-badge-large.png)](https://flattr.com/submit/auto?user_id=kewlbear&url=https://flattr.com/submit/auto?user_id=kewlbear&url=https%3A%2F%2Fgithub.com%2Fkewlbear%2FFFmpeg-iOS-build-script)

This is a shell script to build FFmpeg libraries for iOS and tvOS apps.

Tested with:

* FFmpeg 3.0
* Xcode 7.2.1

## Requirements

* https://github.com/libav/gas-preprocessor
* yasm 1.2.0

## Usage

Use build-ffmpeg-tvos.sh for tvOS.

* To build everything:

        ./build-ffmpeg.sh

* To build arm64 libraries:

        ./build-ffmpeg.sh arm64

* To build fat libraries for armv7 and x86_64 (64-bit simulator):

        ./build-ffmpeg.sh armv7 x86_64

* To build fat libraries from separately built thin libraries:

        ./build-ffmpeg.sh lipo

## Download

You can download a binary for FFmpeg 3.0 release at https://downloads.sourceforge.net/project/ffmpeg-ios/ffmpeg-ios-master.tar.bz2

## External libraries

You should link your app with

* libz.dylib
* libbz2.dylib
* libiconv.dylib

## NOTE
  `--enable-libmp3lame` to support mp3 codec
  event if you installed libmp3lame, the configure file will fail on this requirement, safely comment out that line

## Influences

* https://github.com/bbcallen/ijkplayer/blob/fc70895c64cbbd20f32f1d81d2d48609ed13f597/ios/tools/do-compile-ffmpeg.sh#L7
