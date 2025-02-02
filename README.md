# 🎵 bum

[![PyPI](https://img.shields.io/pypi/v/bum.svg)](https://pypi.python.org/pypi/bum/)
[![MIT licensed](https://img.shields.io/badge/license-MIT-blue.svg)](./LICENSE.md)
[![Build Status](https://travis-ci.org/dylanaraps/bum.svg?branch=master)](https://travis-ci.org/dylanaraps/bum)
[![Donate](https://img.shields.io/badge/donate-patreon-yellow.svg)](https://www.patreon.com/dyla)

`bum` is a daemon that downloads album art for songs playing in `mpd`/`mopidy` and displays them in a little window. `bum` doesn't loop on a timer, instead it waits for `mpd`/`mopidy` to send a `player` event. When it receives a `player` event it wakes up and downloads album art for the current playing track. This makes `bum` lightweight and makes it idle at `~0%` CPU usage.

This fork of `bum` utilizes [sacad](https://pypi.org/project/sacad/) to download the album art based on the artist and album name retrieved from MPD. It is based on the fork https://github.com/jishnusen/bum, but uses MPD instead of PlayerCTL, just like the original version of `bum`.

Note: `bum` is meant to be used with files that don't have embedded album art (`mopidy-spotify`).


![showcase](http://i.imgur.com/uKomDoL.gif)


## Dependencies

- `python 3.6+`
- `python-mpv`
- `python-mpd2`
- `sacad`


## Local installation

```sh
git clone https://github.com/andersonbco/bum.git
cd bum
python3 setup.py install --user
```


## Usage

```sh
usage: bum [-h] [--size "px"] [--cache_dir "/path/to/dir"] [--version]

bum - Download and display album art for mpd tracks.

optional arguments:
  -h, --help            show this help message and exit
  --size "px"           what size to display the album art in.
  --cache_dir "/path/to/dir"
                        Where to store the downloaded cover art.
  --version             Print "bum" version.
  --port                Use a custom mpd port.
```


## Donate

Donations will allow me to spend more time working on `bum`.

If you like `bum` and want to give back in some way you can donate here:

**https://patreon.com/dyla**
