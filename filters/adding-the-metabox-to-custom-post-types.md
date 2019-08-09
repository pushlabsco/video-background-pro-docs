# Adding the Metabox to Custom Post Types

To add the Video Background Pro metabox to a custom post type, add the function below to the bottom of your `functions.php` file. In the `$post_types` array, add your desired custom post types.

```php
<?php
/**
 * Define Video Background Pro's post types
 *
 * @since 1.1.2
 * @author Push Labs
 * @param array $post_types
 * @return array Array of post types Video Background Pro should use
 */
function themeprefix_vidbgpro_post_types( $post_types ) {
  /**
   * list the post types you would like Video Background Pro
   * to use in the form of an array
   */
  $post_types = array( 'post', 'page' );
  return $post_types;
}
add_filter( 'vidbgpro_post_types', 'themeprefix_vidbgpro_post_types' );
```