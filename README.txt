transcode_ch7
Depends: ffmpeg libkate oggz-tools (getopt from util-linux) (dirname from GNU core-utils)
	 [Optional 1] gstreamer >1.6, mkvtoolnix
Usage: transcode_ch7 [options] files...
Options: [--dualaudio|--dualreverse|--keepaudio|--keeprevaudio][--hardsrt[=#]|--hardass[=#]][--sub=#][--externalsrt][--outdir=<path>][--scale][--softdvdsub|--softass]
  dualaudio:    Encodes all audio streams from source in order.
  dualreverse:  Encode both audio streams but swap the order.
  keepaudio:    Just copy audio stream. Use this with videos that already have 
    audio encoded in vorbis (e.g. YouTube videos).
  keeprevaudio: Copy and swap the first two audio streams.
  hardsrt:      Overlay source SRT subtitles into video stream. Optionally
    specify the subtitle stream number.
  hardass:      Overlay source SSA subtitles into video stream. Optionally
    specify the subtitle stream number.
  sub:          Specify the SSA or SRT subtitle stream to encode to kate and
    include with dualaudio (default: 0).
  externalsrt:  Use separate SRT files from source. Subtitle files must have the
    same name as video source file except for file extension.
  outdir:       Set output directory.
  scale:	Scale to pixel height of 480 (DVD resolution)
  softdvdsub:   Transcode source dvdsub into kate. (Added dependencies [1])
  softass:      Use gstreamer to encode SSA directly to kate subtitles. (Depends [1])


ogg-rename-helper
Depends: oggz-tools
Usage: ogg-rename-helper files...
  Appends video duration to file names.

exec_after_transcode
Usage: exec_after_transcode <command to execute>
  For cleanup after multiple instances of transcoding, e.g. unmounting a file 
  share.
