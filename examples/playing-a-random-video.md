# Playing a Random Video Background 

There are some instances where you may want to cycle through a list of videos to be randomly played on page load. This can be dome with a simple function. Paste this at the bottom of the theme's `functions.php` file:

```php
/**
 * Select a random video from an array for the video background.
 *
 * @version 08092019
 * @author Push Labs
 * @link https://pushlabs.co
 */
function theme_prefix_vidbg_random_video() {
    // The page ID in which you want the video background shortcode to be rendered on.
    $page_id = 4;

    // If the page is not the ID specified above, do not render the rest of the code.
    if (!is_page($page_id)) {
        return;
    }

    // Create an array of video files. You will want to replace the values with your own URLs.
    $videos = [
      [
          mp4 => '/video1.mp4',
          webm => '/video1.webm',
      ],
      [
          mp4 => '/video2.mp4',
          webm => '/video2.webm',
      ],
      [
          mp4 => '/video3.mp4',
          webm => '/video3.webm',
      ]
    ];

    // A random array selected from the above $videos array of arrays.
    $get_random_video = array_rand($videos, 1);

    // Add [vidbg] params as needed. Be sure to change the container to your desired container.
    echo do_shortcode('[vidbg container=".YOUR_CONTAINER_HERE" mp4="' . $get_random_video["mp4"] . '" webm="' . $get_random_video["webm"] . '"]');
}
add_action('wp_footer', 'theme_prefix_vidbg_random_video');
```