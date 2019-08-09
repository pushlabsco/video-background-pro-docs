# Adding a Video Background to Every Page

In some instances, you may want a video background on every page of your WordPress site. This is very straight forward thanks to the `[vidbg]` shortcode.

Paste at the bottom of your `functions.php` file:

```php
/**
 * Add a video background to every page/post
 * 
 * @version 05222018
 * @author Push Labs
 * @link https://pushlabs.co
 */
function theme_prefix_vidbg_every_page() {
  // Add [vidbg] params as needed. Be sure to change the container to your desired container.
  echo do_shortcode('[vidbg container=".YOUR_CONTAINER_HERE" mp4="#" webm="#"]');
}
add_action('wp_footer', 'theme_prefix_vidbg_every_page');
```