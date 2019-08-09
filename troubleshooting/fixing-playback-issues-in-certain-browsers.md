 # Fixing Playback Issues in Certain Browsers

 If you notice your self hosted video background playing in one browser but not another, this is likely due to the video files themselves.

 A quick and easy way to determine if the video file itself is at fault, is to open the link to the `.mp4` or `.webm` directly in the browser to see if the video plays. If it does not play, that means that the video files' encoding is not compatible.

 If this is the case, you'll want to re-encode the video files to a codec that is most compatible:

 | File Type | Most Compatible Video Codec | Most Compatible Audio Codec
| - | - | - |
| MP4 | MP4 H.264 Video Codec | AAC Audio Codec
| WebM | VP8 or VP9 Video Codec | Vorbis or Opus Audio Codec

You can [Learn more about optimizing your MP4 here](https://developer.mozilla.org/en-US/docs/Web/HTML/Supported_media_formats#MP4_H.264_(AAC_or_MP3)) or [learn more about optimizing your WebM here](https://developer.mozilla.org/en-US/docs/Web/HTML/Supported_media_formats#WebM).

