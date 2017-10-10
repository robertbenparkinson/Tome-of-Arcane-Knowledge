# How to Create a Photo Gallery

Drupal 8.3.7

Install and Extend the following modules
- Entity
- Entity Browers
- Inline Entity Form
- Media Entity (maybe included in core in Drupal 8.4)
- Media Entity Image (maybe included in core in Drupal 8.4)
- Other modules as needed

## Add new Media Bundle

goto admin/structure/media
- Press "+Add new media bundle" 
- Lable "alex media bundle"
- Description "alex media bundle test"
- Type provider "Image" -- based on the meida types supported
- Field with source information "Image" unable to set until later
- Whether to gather exif data "No"
- File MIME "- Skip field -"
- Width "- Skip field -"
- Height "- Skip field -"
- Publishing options "Published"
- Press "Save Media Bundle"

goto admin/structure/media
- Open media bundle created above
- goto "Manage Fields" Tab
- Press "+ Add field" 
- set Re-Use and existing field to "Image: field_image"
- Label "image"
- Press "Save and continue"
- Label "image"
- Help Text 
- Default Image
- Allowed file extensions
- File directory [current-user:account-name]
-
-
-
- Press "Save Settings"
- goto "Edit" tab
- ensure Field with source information is set to the "Image" field and defined above
- Press "Save Media Bundle"

## Create a New Entity Browser
- goto config/content/entity_browser
- Press 
- Label ""
- Set Display plugin to "iFrame"
- Set Widget selector plugin to "Tabs"
- Set "Selection display plugin" to "No selectoin display"
- Press "Next"
- "Display Page"
- Set "Width of the iFrame" to "650"
- Set "Height of the iFrame" to "500"
- Set "Link text" to "Select entities"
- Check "Auto open entity browser" box
- Press "Next"
- Widget Selector Page
- Press "Next"
- Selection display
- Press "Next"
- Widgets Page
- Set "Add widget plugin" to " - Select a widget to add it - " //this changes ti 
- "Label (Upload)" "Upload images"
- "Submit button text" "Select files"
- "Upload location" ### should I add a token to change location? 
- check "Accept multiple files" box
- "Label (View) "view" 
Allowed file extensions ### currentley set to all, should change
 Submit button text "Select entities"
View : View display set to Entity Browser: Entity browser (Shoud change)


## Create a new Image Style
- goto config/media/image-styles
- press "+ Add image style"




