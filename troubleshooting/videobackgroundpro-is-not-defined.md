---
title: VideoBackgroundPro is not defined
---

# "VideoBackgroundPro" is not defined

If you are experiencing the following error:

```
ReferenceError: VideoBackgroundPro is not defined
```

It means that the plugins main script is not being loaded. This can happen when using optimizing plugins, or caching plugins.

## Autoptimize Conflict Fix

If you are using Autoptimize, and you are experiencing the `ReferenceError` message in the console, you may need to exclude the Video Background Pro scripts from Autoptimize.

Navigate to `WordPress Admin > Settings > Autoptimize`, and find the `Exclude scripts from Autoptimize` input field. You should see something like this in the field:

```
wp-includes/js/dist/, wp-includes/js/tinymce/, js/jquery/jquery.js
```

You'll want to include the `VideoBackgroundPro.js` script in the field. Update the field to:

```
wp-includes/js/dist/, wp-includes/js/tinymce/, js/jquery/jquery.js, wp-content/plugins/video-background-pro/dist/VideoBackgroundPro.js
```

Finally, be sure to click the button at the bottom `Save Changes and Empty Cache`