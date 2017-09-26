# DRUPAL 8 BootStrap Subtheme

## Implement the following steps
1. download current Bootstrap Theme from Drupal.org site
2. Install them through Drupal API or just unzip and stuff file into /theme file
3. open /bootstrap and find /starterkit
4. open /starterkit and copy /cdn file
5. move /cdn folder to /theme folder (how ever you have it organized)
6. rename to /cdn folder to /YOUR_THEME_NAME
7. remane THEMENAME.libraries.yml to YOUR_THEME_NAME.libaries.yml
8. remane THEMENAME.theme to YOUR_THEME_NAME.theme
9. remane THEMENAME.starterkit.yml to YOUR_THEME_NAME.info.yml
10. open OUR_THEME_NAME.info.yml
11. change "name: 'THEMENAME'" to "name: 'YOUR_THEME_NAME'"
12. update  "description:" key 
13. update "libraries:" key to 'YOUR_THEME_NAME/global-styling'
14. save file
15. open /YOUR_THEME_NAME/config/install folder and rename THEMENAME.setttings.yml file to YOUR_THEME_NAME.settings.yml
16. open /YOUR_THEME_NAME/config/schema folder and rename THEMENAME.schema.yml file to YOUR_THEME_NAME.schema.yml
17. open YOUR_THEME_NAME.schema.yml file and update "THEMENAME.settings:" key to read "YOUR_THEME_NAME.settings:
18. update "label:" key with your themes label
19. save YOUR_THEME_NAME.schema.yml
20. Clear your cache and install YOUR_THEME_NAME through either the API or DRUSH

## Warnings
- Watch your spelling. TWIG is case sensitive 
- DO NOT TAB. TWIG is sensitive to that too!
- TWIG may also have a gluten allergy 

If you run aross the error "Can't install module because configuration already exists in active configuration" try uninstalling the module and then reinstallings.
If that doesn't work try going to your sites databases, look in the config table and delete the deleting the YOUR_THEME_NAME.settings record from the database. 

## CSS Overrides
place all css over rides in YOUR_THEME_NAME/css/style.css
