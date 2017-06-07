# Building an New Drupal 8 Theme

## Set Up Development Environment
1. Copy and move <b>example.settings.local.php</b> file from <b>sites/</b>  folder to <b>sites/default</b> folder
2. Rename <b>example.settings.local.php</b> file to <b>settings.local.php</b>
3. Open <b>settings.php</b> file in <b>sites/default</b> folder and uncomment the following lines...
```php
 if (file_exists($app_root . '/' . $site_path . '/settings.local.php')) {
   include $app_root . '/' . $site_path . '/settings.local.php';
 }
 ```
 4. Open <b>settings.local.php</b> file and check to see if <b>css</b> and <b>js</b> aggreagion has been turned off
 ```php
$config['system.performance']['css']['preprocess'] = FALSE;
$config['system.performance']['js']['preprocess'] = FALSE;
## FALSE == OFF
## TRUE == ON
```
5. Next uncomment the following two lines of code in <b>settings.local.php</b> file
```php
$settings['cache']['bins']['render'] = 'cache.backend.null';
$settings['cache']['bins']['dynamic_page_cache'] = 'cache.backend.null';
```
6. Next turn off test modules and themes by setting the following lines of code to FALSE
```php
$settings['extension_discovery_scan_tests'] = TRUE;
```
7. Save file and Drush CR.
