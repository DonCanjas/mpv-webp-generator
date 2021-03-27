# mpv-webp-generator *for windows*
Creates high quality animated webp using mpv hotkeys

![Fruits Basket Season 2](https://files.catbox.moe/rt0czz.webp)

Based on [Scheliux](https://github.com/Scheliux/)'s [gif generator](https://gist.github.com/Ruin0x11/8fae0a9341b41015935f76f913b28d2a) port to windows, which you cand find [here](https://github.com/Scheliux/mpv-gif-generator).

Thanks to July who helped me with ffmpeg's parameters.

# Requirements 
- Windows
- mpv
- ffmpeg

# Installation

First of all, you must make sure `ffmpeg` is in your `%PATH%` and accesible via your command line. After ensuring this, clone or download as zip. Then, head to `%APPDATA%/mpv/scripts` and place `mpv-webp.lua` in there; if neither `%APPDATA%/mpv` nor `%APPDATA%/mpv/scripts` exist, you will have to create them. It's as easy as that!

[How to install ffmpeg](https://www.wikihow.com/Install-FFmpeg-on-Windows)

# Configuration
*Note this is still in progress and might not work properly*

The three options the script offers (at least until now) are:

* `dir` – Sets the output directory. Default is `C:/Program Files/mpv/webp/`.
* `rez` – Sets the resolution of the output webp. Default is 600 width.
* `fps` – Sets the framerate of the output webp. Default is 15. Don't go too overboard or the filesize will balloon.

# webp settings
* `qscale` - set as 90 out of 100. It will determine the quality of the webp. Not recommended to go lower than 85. 
* `lossless` - set as 0 by default (lossy), change to 1 for lossless. When doing a lossless export, `qscale` will no longer determine the quality, but the encoding eficiency.
* `compression_level` - set as 6 out of 6. The process might take a while, so if you don't want to wait, you should lower it, but the lower the value, the bigger the filesize.
* `preset` - `none` is the default. You can also switch to `default`, `picture`, `photo`, `drawing`, `icon` and `text`. [FFmpeg's documentation on webp's presets](https://ffmpeg.org/ffmpeg-codecs.html#toc-Options-30).

## Usage
You can use `,` and `.` to rewind or foward one frame at a time in order to select the desired starting and ending frames of the webp. You only need to define the start and ending times and to choose if exporting with or without subtitles. In order to do that, you can use the following hotkeys: 

* `w` - Start time
* `W` - End time
* `CTRL+w` - Export webp
* `CTRL+W` - Export webp with subtitles  - *only works with srt*

## Stuff to do
If you wish to contribute, here are some suggestions:

* Add support for ass/ssa hardsubbing while keeping its styles, hardsubbing the track the user has selected on mpv;
* Add support for a config file to customize not only webp's settings, but also keybindings and output directory. (at least I can't make it work on my pc)
