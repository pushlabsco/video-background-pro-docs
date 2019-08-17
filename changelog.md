---
title: Changelog
description: All of the changes in Video Background Pro
---

# Changelog

## v4.0.3 (Aug 17, 2019)
### Enhancements
* Added the `vidbgpro_player_do_not_track` filter. This filter allows you to disable tracking (cookies) from the YouTube and Vimeo players. [View the documentation on this feature here.](http://docs.pushlabs.co/video-background-pro/filters/do-not-track-cookies/)

## v4.0.2 (Aug 15, 2019)
### Bug Fixes
* Fixed an issue where the video background size was larger than intended when using the "body" container

## v4.0.1 (Jul 6, 2019)
### Bug Fixes
* Fixed an issue with WPBakery integration where video backgrounds would not display when using a self hosted video background.

## v4.0.0 (Jun 24, 2019)
### Enhancements
* Video Background Pro has been completely rewritten in ES6+ JavaScript. This means no more reliance on dependencies like jQuery. This should make the plugin much faster!
* The plugin can now play video backgrounds on any device that supports HTML5 `<video>`. This means any modern mobile device will play video backgrounds on any browser with Video Background Pro.
* Vimeo video backgrounds are here! Paste your Vimeo video URL into the "Vimeo URL" field just like the YouTube integration.
* Fallback image now displays indefinitely until the video starts playing. This not only looks better, but is more consistent on devices that do not support auto-playing video.
* Video backgrounds now have a subtle fade-in once they start playing.
* The fallback/poster image is now added through PHP instead of the JavaScript plugin in order to immediately display the image, instead of after page load when JavaScript starts to run.
* Added the `player_options` flag to the `[vidbg]` shortcode. This allows you to supply your own arguments to the HTML5 `<video>` tag or to the YouTube/Vimeo players! The value for the `player_options` flag must be a JSON string.
* Added the `frontend_container` flag to the `[vidbg]` shortcode. This allows you to position the front-end buttons wherever you like in the case that the current placement doesn't work with your theme.
* Video Background Pro will support all modern browsers, and Internet Explorer 11.

### Bug Fixes
* Fixed an issue where YouTube videos would not load if scrolling rapidly upon page load.
* Non numeric inputs for YouTube start and end seconds no longer crash the plugin.

### Depreciations
* `Overlay Texture` option is now depreciated as of 4.0.0. It will no longer be an option in the shortcode, metabox, or integrations.
* `Enable Loader` option is now depreciated as of 4.0.0 in place of the fallback image now displaying until the video is ready to play. It will no longer be an option in the shortcode, metabox, or integrations.
* `play_on_mobile` shortcode flag is depreciated as of 4.0.0. Video Background Pro will now play the video background on any device that supports auto-playing videos.

## v3.0.2 (Jun 9, 2018)
* Fixed: Issue with front end buttons and end frame poster on SiteOrigin integration.

## v3.0.1 (May 11, 2018)
* Fixed: string(27) "no self hosted video exists" error messages when no video is present using SiteOrigin

## v3.0.0 (May 7, 2018)
* Enhancement: Completely rewrote Visual Composer integration class. Now reliable across all different themes/plugins.
* Removed: Old Visual Composer data model for more reliable one. UPGRADING TO 3.0.0 WILL REQUIRE YOU TO RE-ENTER YOUR VIDEO BACKGROUND INFORMATION FOR ALL VISUAL COMPOSER INTEGRATION INSTANCES.
* Enhancement: Completely rewrote SiteOrigin integration class. Now reliable across all different themes/plugins.
* Removed: Old SiteOrigin data model for more reliable one. UPGRADING TO 3.0.0 WILL REQUIRE YOU TO RE-ENTER YOUR VIDEO BACKGROUND INFORMATION FOR ALL SITEORIGIN INTEGRATION INSTANCES.
* Removed: Ability to autoplay video backgrounds with sound as it was breaking video backgrounds due to browsers new standards for autoplaying videos.
* Added: vidbgpro_update_message() to quickly see what is included in a Video Background Pro update from the WordPress plugins screen.
* Removed: vidbgpro_is_wp_version()
* Removed: vidbgpro_loader_colors()
* Added: Debug mode to easily debug video backgrounds if WP_DEBUG is set to true
* Added: vidbgpro_enable_siteorigin() filter to disable SiteOrigin Integration if desired
* Added: vidbgpro_integration_use_old_data_model() filter to use old integration classes if desired (not recommended)

## v2.4.1 (Mar 24, 2018)
* Fixed: Undefined property Notice regarding $ame_getting_started

## v2.4.0 (Mar 24, 2018)
* Added: Feature - Loader Fallback Background: You can now display your fallback image as the loader background!
* Fixed: An issue regarding the <script> tag in wp_add_inline_script()

## v2.3.2 (Mar 8, 2018)
* Fixed: Cleaned up some code comments
* Added: function to delete Video Background Pro transients on deactivation
* Removed: API Activation is no longer required to use the plugin's features, but is still required in order to get updates and support.

## v2.3.1 (Mar 4, 2018)
* Added: If page has window.onYouTubePlayerAPIReady(), Video Background Pro will combine the function with Video Background Pro's to avoid conflicts
* Added: console.log() flags for testing

## v2.3.0 (Mar 2, 2018)
* Added: Public method to play video background .playVidbg()
* Added: Public method to pause video background .pauseVidbg()
* Added: Public method to mute video background .muteVidbg()
* Added: Public method to unmute video background .unMuteVidbg()
* Added: Public method to resize video background .resizeVidbg()
* Added: Plugin init calls are now added to the page using wp_add_inline_script()
* Removed: Depreicated [vidbgpro] shortcode

## v2.2.0 (Feb 14, 2018)
* Added: play_on_mobile shortcode option. Accepts true/false.
* Added: vidbgpro_script_deps() allows to add deps to Video Background Pro script
* Added: vidbgpro_enable_vc() filter for disabling Visual Composer integration
* Added: vidbgpro_play_on_mobile_default() filter for default mobile playback behavior

## v2.1.1 (Sep 25, 2017)
* Fixed: Removed old admin page

## v2.1.0 (Sep 24, 2017)
* Fixed: compatibility issue in High Sierra and IOS 11
* Added: Video playback on supported mobile devices!
* Added: License authentication for OTA plugin updates

## v2.0.0 (Jul 9, 2017)
* Major changes have been brought to v2 to better optimize the plugin and offer more features
* Fixed: Completely rewrote vidbg into one clean script to handle all functionality. More optimized and error free.
* Fixed: Issues experienced on some mobile devices.
* Fixed: open_basedir() issue some users were experiencing
* Added: Now .zip is just the WordPress installable. Just download and upload to get started.
* Added: Feature - Youtube Start Second
* Added: Feature - Youtube End Second
* Added: Feature - End video on fallback.
* Added: Feature - Custom CSS loader for self host and Youtube
* Fixed: Overlay not showing on mobile devices
* Fixed: All instances of Video Background Pro are now ran straight from the shortcode for more consistency.
* Fixed: Video Background Pro now will only call all YouTube elements if a YouTube video background instance exists to lower the risk of conflict
* Fixed: You can now add any YouTube video link type to the shortcode, metabox, etc.
* Fixed: All CSS was moved to an independent CSS file for faster loading and appearance.
* Added: Video backgrounds now load much faster due to better coding and optimization.
* Added: vidbgpro_metabox_priority() filter for changing the priority of the Video Background Pro metabox.
* Fixed: Video or iframe element will no longer be created and added to the page if mobile is detected for less clutter and faster load speeds.
* Fixed: YouTube videos will now load much faster now that you have the ability to toggle the CSS loader.

## v1.1.4 (Aug 3, 2016)
* Added: Better mobile device support.
* Added: Support for iPad Pro.
* Fixed: Issue with video showing in top left-hand area of screen before being resized.
* Fixed: License URLs

## v1.1.3 (Aug 2, 2016)
* Fixed: Issue with placeholder image showing up before the video
* Fixed: Slow video delay
* Added: Combined JS files for less http requests and faster load times

## v1.1.2 (Jul 12, 2016)
* Fixed compatibility issue with CMB2
* Added filter to change loader background color
* Added a post type filter to add new post types to VBP
* Fixed a display issue for YouTube videos when container was set to "body"
* Added frontend buttons position option
* Fixed an issue where the fallback image would show up before the video played

## v1.1.1 (Jun 21, 2016)
* Add localized text for backend
* Added preventDefault to advanced button
* Replaced spaces with tabs
* Added new [vidbg] shortcode. The [vidbgpro] shortcode is now deprecated

## v1.1.0 (Jun 9, 2016)
* Fixed an issue with the looping option when using the YouTube integration.

## v1.0.0 (Jun 5, 2016)
* Initial Release
