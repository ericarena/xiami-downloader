# Xiami Music Preview Downloader

A simple tool for downloading music previews from [Xiami.com][1]

Note: this is a python script using python 2.

## Usage

    xiami.py [options]

## Options

* `-a <album id>` Adds all songs in an album to download list.
* `-p <playlist id>` Adds all songs in a playlist to download list.
* `-s <song id>` Adds a song to download list.
* `-t urllib2|wget` Change the download tool.
* `-h` Shows usage.

`<song id>`, `<playlist id>` and `<album id>` can be retrived from URLs of Xiami.

Default download tool is the built-in urllib2 on Windows, others will be wget.

## Example

To download the album _Mahōtsukai no Yoru OST_, first refer to the url <http://www.xiami.com/album/511682> to get album ID: __511682__. Then use the following command to download:

    xiami.py -a 511682

[1]: http://www.xiami.com "虾米"
