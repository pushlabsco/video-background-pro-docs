---
title: Using the Shortcode
description: Everything about the [vidbg] shortcode
---

# Using the Shortcode

<div style="padding-top: 56.25%; position: relative;">
    <iframe style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;" src="https://www.youtube.com/embed/Ax-MSgWP5ww" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

The shortcode is the backbone of the entire Video Background Pro plugin. Whether or not you realize it, every other way to create a video background (metabox, WPBakery, SiteOrigin) all end up using the shortcode to initialize the plugin and add it to your website.

## Parameters

The shortcode has parameters that you can specify to tailor your video background experience.

**It's important to note that due to the way that shortcodes are implemented, every value is interpreted as a string.**

| Parameter | Description | Type | Accepts | Default Value
| -|-| -| -| -|
| container | The container value. This is where your video background will go. This parameter is required. | Any | Any DOM Element | `""`
| type | The type of video background you would like. | Any | self-host, youtube, vimeo | "self-host"
| mp4 | The .mp4 file link. | `self-host` | Any URL with an `.mp4` file extension. | "null"
| webm | The .webm file link. | `self-host` | Any URL with a `.webm` file extension. | "null"
| youtube_url | The YouTube URL. Can be any type of YouTube URL (shortened, regular, embed, etc).| `youtube` | Any YouTube video URL. | "null"
| youtube_start | The YouTube video background start second. This must be a number, not the minutes and seconds. For example, if you want the video to start at 1:32, you would input 92. | `youtube` | A number less than the total amount of seconds in the YouTube video. | "0"
| youtube_end | The YouTube video background end second. This must be a number, not the minutes and seconds. For example, if you want the video to end at 1:32, you would input 92. | `youtube` | A number less than the total amount of seconds in the YouTube video. | "null"
| vimeo_url | The Vimeo video URL. | `vimeo` | A Vimeo Video URL ex. https://vimeo.com/xxxx where "xxxx" is the ID. | "null"
| poster | The poster image will be shown while the video is loading and for devices/browsers that do not support video backgrounds. | Any | Any URL to an image. .png and .jpg are recommended. | "null"
| end\_frame\_poster | This option will add the poster image to the video background once it stops playing. The `loop` parameter must be set to `false` for this to work. | Any | `true` or `false` | "false"
| muted | This option has been depreciated due to browser restrictions. As of Video Background Pro 3.0.0 this option will no longer do anything. | Any | `true` or `false` | "true"
| loop | This option will dictate whether or not the video background will loop. | Any | `true` or `false` | "true"
| overlay | To enable the overlay or not. | Any | `true` or `false` | "false"
| overlay_color | Specify the color of the overlay as a hex color. The `overlay` parameter must be set to `true` for this to take effect. | Any | Any Hex color. | "#000"
| overlay_alpha | Specify the amount of transparency your overlay will have. This can be useful for text legibility. | Any | A value between `0.00` and `1.00` where `0.00` is completely transparent and `1.00` begin opaque. | "0.3"
| overlay\_texture\_url | This option was depreciated in Video Background Pro 4.0.0, and will no longer do anything. | Any | Any URL to an image. | "#"
| frontend\_play\_button | Toggle a play/pause button for the video background. | Any | `true` or `false` | "false"
| frontend\_volume\_button | Toggle a mute/unmute button for the video background. | Any | `true` or `false` | "false"
| frontend_position | Specify the position of the frontend buttons. Either `frontend_play_button`, `frontend_volume_button` or both must be enabled. | Any | `bottom-right`, `bottom-left`, `top-right`, `top-left` | "bottom-right"
| enable_loader | This option was depreciated in Video Background Pro 4.0.0, and will no longer do anything. | Any | `true` or `false` | "false"
| play\_on\_mobile | This option was depreciated in Video Background Pro 4.0.0, and will no longer do anything. Now, the video background will play on any mobile browser that supports HTML5 `<video>`. | Any | `true` or `false` | "true"
| player_options | Allows you to interact with the player's API. Can be used for `self-host`, `youtube`, and `vimeo` video backgrounds. Make a JSON string of an object with the options that you would like to add/override. | Any | A JSON String with an object of key:value pairs. | "null"
| frontend_container | Use this option if you'd like to re-position your frontend buttons. Used just like the `container` parameter, simply provide a DOM element for it to be moved to. | Any | Any DOM Element | "null"

## Constructing the Shortcode

When you are constructing the shortcode, you only need to add the parameters that matter to you. In this instance, say we have a container `.my-section-5` and we want a YouTube video background of [Rick Astley's "Never Gonna Give You Up"](https://www.youtube.com/watch?v=dQw4w9WgXcQ). Our shortcode would look something like this:

```
[vidbg container=".my-section-5" type="youtube" youtube_url="https://www.youtube.com/watch?v=dQw4w9WgXcQ"]
```