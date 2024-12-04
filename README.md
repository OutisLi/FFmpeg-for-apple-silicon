# FFmpeg Build Script for Apple Silicon

This script is based on [OSXExperts.NET Guide](https://www.osxexperts.net) and [ssut's ffmpeg-on-apple-silicon Project](https://github.com/ssut/ffmpeg-on-apple-silicon).

Thanks to these two projects, I've successfully built FFmpeg on my M4 Pro Mac mini.

Notes:
- This script only involves essential packages. If you need more packages, please refer to the original projects.
- It should be enough for daily use without the need for burded in captions.


```bash
$ ./ffmpeg
ffmpeg version git-2024-12-04-7c1e732 Copyright (c) 2000-2024 the FFmpeg developers
  built with Apple clang version 16.0.0 (clang-1600.0.26.4)
  configuration: --prefix=/Users/outisli/Project/ffmpeg-on-apple-silicon/workdir/sw --extra-cflags=-fno-stack-check --arch=arm64 --cc=/usr/bin/clang --enable-gpl --enable-libopus --enable-libmp3lame --disable-ffplay --enable-libx264 --enable-libx265 --enable-libvpx --enable-postproc --enable-libsnappy --enable-version3 --pkg-config-flags=--static --enable-nonfree --enable-runtime-cpudetect --enable-libsvtav1 --enable-videotoolbox --enable-audiotoolbox --enable-libvmaf
  libavutil      59. 47.101 / 59. 47.101
  libavcodec     61. 26.100 / 61. 26.100
  libavformat    61.  9.100 / 61.  9.100
  libavdevice    61.  4.100 / 61.  4.100
  libavfilter    10.  6.101 / 10.  6.101
  libswscale      8. 12.100 /  8. 12.100
  libswresample   5.  4.100 /  5.  4.100
  libpostproc    58.  4.100 / 58.  4.100
Universal media converter
usage: ffmpeg [options] [[infile options] -i infile]... {[outfile options] outfile}...

Use -h to get full help or, even better, run 'man ffmpeg'


$ lipo -archs ffmpeg
arm64
```

## Guide

Before you start you must install arm64-based Homebrew to `/opt/homebrew`.

1. Clone this repository.
2. Run `./build.sh`.
