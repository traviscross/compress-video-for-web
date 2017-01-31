# compress-video-for-web

This is a tool for compressing videos in a way that most devices can
play them from web browsers.  It uses the excellent `ffmpeg` tool.

## Usage

    ./compress-video-for-web [options] <in-files>

Options include:

`-a <audio-bitrate>` Sets the audio bitrate it bits/second.  Accepts
suffixes supported by `ffmpeg` such as `k` or `M`.

`-c` Indicates whether to concatenate the `<in-files>` together into
one video or to compress them independently.

`-f <format>` Specifies the output format.  Currently supported are
`webm` and `mp4`.

`-m <framerate>` Sets the framerate for the output video.  The default
is `29.97`.

`-r <resolution>` Sets the output resolution.  Currently supported are
`480` (hd480), `720` (hd720), `1080` (hd1080), `2048` (2k), and `4096`
(4k).

`-v <video-bitrate>` Sets the video bitrate in bits/seconds.  Accepts
suffixes supported by `ffmpeg` such as `k` or `M`.

## Output

The output of this tool is stored in a file that's the same as the
output file minus the prefix with a suffix of
`_<resolution>p_wq.<format>`.  The `wq` stands for "web quality.

## Dependencies

This tool is designed to run under a POSIX-style shell such as `dash`.
The tool relies on `ffmpeg` being installed.

## License

This project is licensed under the
[MIT/Expat](https://opensource.org/licenses/MIT) license as found in
the [LICENSE](./LICENSE) file.
