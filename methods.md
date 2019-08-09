# Using Methods

Methods allow you to execute certain actions on your video background instance. Current methods provide the ability to play, pause, mute, unmute, and resize a video background.

```js
// Be sure to use your own container!
var container = '.your-container'

// Method to play a video background
jQuery(container).data('vidbgpro').playVidbg();

// Method to pause a video background
jQuery(container).data('vidbgpro').pauseVidbg();

// Method to mute a video background
jQuery(container).data('vidbgpro').muteVidbg();

// Method to unmute a video background
jQuery(container).data('vidbgpro').unMuteVidbg();

// Method to resize a video background
jQuery(container).data('vidbgpro').resizeVidbg();
```

It is important to make sure you call these methods after Video Background Pro has initialized.