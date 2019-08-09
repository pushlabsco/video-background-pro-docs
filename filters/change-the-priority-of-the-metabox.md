# Change the Priority of the Metabox

If you would like to change the position of the Video Background Pro metabox, you can achieve this through a filter. Add the function below to the end of your `functions.php` file. In the `$priority` variable, define the priority.

```php
<?php
/**
 * Define Video Background Pro's metabox priority
 *
 * @since 2.0.0
 * @author Push Labs
 * @uses apply_filters()
 * @return string The location of the metabox used by WordPress
 * @link https://developer.wordpress.org/reference/functions/add_meta_box/
 */
function themeprefix_vidbgpro_metabox_priority( $priority ) {
  /**
   * The metabox priority. For more information refer to:
   * @link https://developer.wordpress.org/reference/functions/add_meta_box/
   */
  $priority = 'high';
  return $priority;
}
add_filter( 'vidbgpro_metabox_priority', 'themeprefix_vidbgpro_metabox_priority' );
```