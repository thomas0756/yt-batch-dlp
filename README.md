# yt-batch-dlp
This is a simple script to automate downloading and transcoding a long list of video URLs using yt-dlp and ffmpeg. It downloads then transcodes each video individually to make interrupting and resuming long lists easier.

There are two presets available for the container and codecs:
- legacy - wide compatibility (H.264 video, AAC audio, MP4 container)
- modern - better size and quality (AV1 video, Opus audio, WebM container)

The script has options to set resolution, output path, codec preset and other useful options:
|||
|---|---|
|-f| Path to list of URLs to download (required) |
|-o| Output directory (required) |
|-p| Preset (defaults to legacy) |
|-r| Resolution and framerate, in the format \<height>@\<framerate> (defaults to 1080@60) |
|-b| Browser to import cookies from, same as yt-dlp's list |

<br>
⚠️ Currently only hardware acceleration using VAAPI is supported by the script, though this might change in the future.
