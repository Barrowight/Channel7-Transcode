transcode_ch7
Depends: ffmpeg libkate oggz-tools (getopt from util-linux) (dirname from GNU core-utils)
Usage: transcode_ch7 [options] files...
Options: [--dualaudio|--dualreverse|--keepaudio|--keeprevaudio][--hardsrt[=#]|--hardass[=#]][--sub=#][--softdvdsub|--softass][--externalsrt][--outdir=<path>]
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
  softdvdsub:   Transcode source dvdsub into kate. (Note: This currently
    requires a custom build of gstreamer 1.4.5 with patches from their bug
    tracker [1].
  softass:      Use gstreamer to encode SSA directly to kate subtitles. [1]
  externalsrt:  Use separate SRT files from source. Subtitle files must have the
    same name as video source file except for file extension.
  outdir:       Set output directory.

[1] https://bugzilla.gnome.org/show_bug.cgi?id=740565

ogg-rename-helper
Depends: oggz-tools
Usage: ogg-rename-helper files...
  Appends video duration to file names.

exec_after_transcode
Usage: exec_after_transcode <command to execute>
  For cleanup after multiple instances of transcoding, e.g. unmounting a file 
  share.
