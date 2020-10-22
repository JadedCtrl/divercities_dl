================================================================================
DIVERCITIES_DL                                              get those bits local
================================================================================
divercities_dl is a download script for Divercities, a pretty good (but bloated)
music site. It can download entire albums, preserving metadata, or it can
download individual tracks (without metadata).

----------------------------------------
REQUIREMENTS
----------------------------------------
* ksh, bash, etc
* jq      (https://stedolan.github.io/jq/)
* lynx    (https://lynx.browser.org/)
* ffmpeg  (https://ffmpeg.org/)
* a divercities account

Before using divercities_dl, you need to log into Divercities from your
web-browser, and copy the value of the '_divercities_session' cookie into
the $DC_COOKIE environment variable.
Otherwise, authorization will fail, and downloading tracks will be impossible.


----------------------------------------
USAGE
----------------------------------------
Use the `-a` argument followed by a URL or ID to download an album.

By default, tracks are downloaded at the highest bitrate available. To use
the low bitrate option, use the `-l` argument.

By default, when downloading an album, it will download each track like this:
	./artist/album/track.mp3
	./artist/album/track.json

The JSON file contains all (public) metadata that Divercities had on the track,
which is mostly useless, except for archival purposes.

You can disable this format (and instead dump tracks in the current directory)
with the `-s` argument.

The `-h` argument prints the program's Usage message.


----------------------------------------
BORING STUFF
----------------------------------------
License is GPLv3.
jadedctrl@teknik.io
