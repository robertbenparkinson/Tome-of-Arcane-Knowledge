# Set Up Local Environment 


## Create local settings files
Go to sites folder  
copy **examples.settings.local.php** file  
move file to **sites/default** folder  
rename file to **settings.local.php**  
open **settings.php** file in **sites/default** folder  
change **settings.php** from read-only 
uncomment the if statement that will allow **settings.local.php** file (towards the bottom of the file)  
save **settings.php** file  

## Disable CSS and JS Aggregation 
open **settings.local.php** file located in **sites/default** folder  
set both CSS and JS aggregation config statements to TRUE  
**$config['system.performance']['css']['preprocess'] = TRUE;**  
**$config['system.performance']['js']['preprocess'] = TRUE;**  

## Disable render and page cache
uncomment the **$settings['cache']['bins']['render'] = 'cache.backend.null';** line.  
uncomment the **$settings['cache']['bins']['dynamic_page_cache'] = 'cache.backend.null';**  

## Disable test modules and themes
set **$settings['extension_discovery_scan_tests'] = TRUE;** to **False** 
save the **settings.local.php** file.  

##Enable Twig debugging
go to **sites/default** folder  
copy and rename **default.services.yml** file to **services.yml**  
open **services.yml** file  
set the following statements 
```yml
twig.config: 
  debug : true  
  auto_reload : true  
  cache : false
```
save **services.yml** file  
