# Lollypop 

## Codec support
You can use proprietary codecs like [.wma](https://en.wikipedia.org/wiki/Windows_Media_Audio) and [.ra](https://en.wikipedia.org/wiki/RealAudio) by using an optional extension provided by FFmpeg.

To install the extension, run the following command:

```
flatpak install flathub org.freedesktop.Platform.ffmpeg-full//21.08
```

## Platform support
With the release of Lollypop 1.4.8, the sandboxing of Lollypop has been improved. Sadly, this requires Flatpak 1.8.x or higher, which is not available on all platforms by default.

### Ubuntu derivatives
For Ubuntu 18.04 and 20.04, you must add the official PPA so that flatpak can be properly updated:

```
$ sudo add-apt-repository ppa:alexlarsson/flatpak
$ sudo apt update
$ sudo apt install flatpak
``` 

### Other options
You can also remove the additional sandboxing by reverting the sandboxing altogether:

```
flatpak override --user org.gnome.Lollypop --filesystem=host
```