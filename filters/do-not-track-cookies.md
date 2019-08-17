---
title: Turn Off Tracking (Cookies)
description: How to disable tracking and cookies in the YouTube and Vimeo players
---

# Turn Off Tracking (Cookies)

If you would like to disable tracking and cookies from the YouTube and Vimeo players, you can do so with a filter. This is a global filter, meaning that by using this filter, tracking and cookies will turn off across all video background instances on your site.

Add the function below to the end of your `functions.php` file. 

```php
/**
 * Turn off tracking and cookies for YouTube and Vimeo players in Video Background Pro.
 *
 * @since 4.0.3
 * @author Push Labs
 * @uses apply_filters()
 * @return Boolean True or false to turn off tracking.
 */
function themeprefix_vidbgpro_player_do_not_track( $do_not_track ) {
  // True will turn off all tracking and cookies for the players.
  $do_not_track = true;

  return $do_not_track;
}
add_filter( 'vidbgpro_player_do_not_track', 'themeprefix_vidbgpro_player_do_not_track' );

```