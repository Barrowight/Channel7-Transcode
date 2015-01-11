transcode_ch7
Depends: ffmpeg libkate oggz-tools
Usage: transcode_ch7 [options] files...
Options: [--keepaudio|--dualaudio|--dualreverse|--hardsrt|--hardass][--sub=#][--externalsrt]
  keepaudio:    Just copy audio stream. Use this with videos that already have 
    audio encoded in vorbis (e.g. YouTube videos).
  dualaudio:    Encodes all audio streams from source in order.
  dualreverse:  Encode both audio streams but swap the order.
  hardsrt:      Overlay source SRT subtitles into video stream.
  hardass:      Overlay source SSA subtitles into video stream.
  sub:          Specify the subtitle track to operate on (default: 0).
  externalsrt:  Use separate SRT files from source. Subtitle files must have the
    same name as video source file except for file extension.

ogg-rename-helper
Depends: oggz-tools
Usage: ogg-rename-helper files...
  Appends video duration to file names.

exec_after_transcode
Usage: exec_after_transcode <command to execute>
  For cleanup after multiple instances of transcoding, e.g. unmounting a file 
  share.
