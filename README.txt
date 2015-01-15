transcode_ch7
Depends: ffmpeg libkate oggz-tools
Usage: transcode_ch7 [options] files...
Options: [--keepaudio|--dualaudio|--dualreverse][--hardsrt[=#]|--hardass[=#]][--sub=#][--externalsrt][--outdir=<path>]
  keepaudio:    Just copy audio stream. Use this with videos that already have 
    audio encoded in vorbis (e.g. YouTube videos).
  dualaudio:    Encodes all audio streams from source in order.
  dualreverse:  Encode both audio streams but swap the order.
  hardsrt:      Overlay source SRT subtitles into video stream. Optionally
    specify the subtitle stream number.
  hardass:      Overlay source SSA subtitles into video stream. Optionally
    specify the subtitle stream number.
  sub:          Specify the ssa or srt subtitle stream to encode to kate and
    include with dualaudio (default: 0).
  externalsrt:  Use separate SRT files from source. Subtitle files must have the
    same name as video source file except for file extension.
  outdir:       Set output directory.

ogg-rename-helper
Depends: oggz-tools
Usage: ogg-rename-helper files...
  Appends video duration to file names.

exec_after_transcode
Usage: exec_after_transcode <command to execute>
  For cleanup after multiple instances of transcoding, e.g. unmounting a file 
  share.
