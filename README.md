# mpv-webp-generator *for windows*
Creates high quality animated webp using mpv hotkeys

![Fruits Basket Season 2](https://files.catbox.moe/rt0czz.webp)

Based on [Scheliux](https://github.com/Scheliux/)'s gif generator port to windows, which you cand find [here](https://github.com/Scheliux/mpv-gif-generator).

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

After setup, and if you wish, create a `%APPDATA%/mpv/script-opts` directory if it isn't created already and write a `webp.conf` file to configure the script. The three options the script offers (at least until now) are:

* `dir` – Sets the output directory. Default is `C:/Program Files/mpv/webp/`.
* `rez` – Sets the resolution of the output webp. Default is 600 width.
* `fps` – Sets the framerate of the output webp. Default is 15. Don't go too overboard or the filesize will balloon.

# webp settings
* `qscale` - set as 90 out of 100. It will determine the quality of the webp. Not recommended to go lower than 85. 
* `lossless` - set as 0 by default (lossy), change to 1 for lossless. When doing a lossless export, `qscale` will no longer determine the quality, but the encoding eficiency.
* `compression` - set as 6 out of 6. The process might take a while, so if you don't want to wait, you should lower it.

## Hotkeys

* `w` - Start time
* `W` - End time
* `CTRL+w` - Export webp
* `CTRL+W` - Export webp with subtitles *only works for srt*
