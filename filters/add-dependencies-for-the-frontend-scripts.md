# Add Dependencies for the Frontend Scripts

A theme or plugin may be conflicting with Video Background Pro. In that case, you could require Video Background pro to enqueue after those plugin/theme scripts to avoid any conflicts using the filter below:

```php
<?php
/**
 * Define Video Background Pros Script Dependencies
 *
 * @since 2.2.0
 * @author Push Labs
 * @param Array $deps The dependencies for the Video Background Pro plugin
 * @return Array $deps
 */
function themeprefix_vidbgpro_deps( $deps ) {
  $deps = array( 'jquery' );
  return $deps;
}
add_filter( 'vidbgpro_script_deps', 'themeprefix_vidbgpro_deps' );
```