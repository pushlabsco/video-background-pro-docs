# Disable the WPBakery Integration

If you need to disable the WPBakery (Visual Composer) integration, you could disable it using the following filter:

```php
<?php
/**
 * Disable Video Background Pro's Visual Composer Integration
 *
 * @since 2.2.0
 * @author Push Labs
 * @param Boolean $is_enabled Boolean decisison to enable/disable the integration
 * @return Boolean $is_enabled
 */
function themeprefix_vidbgpro_disable_vc( $is_enabled ) {
  $is_enabled = false;
  return $is_enabled;
}
add_filter( 'vidbgpro_enable_vc', 'themeprefix_vidbgpro_disable_vc' );
```