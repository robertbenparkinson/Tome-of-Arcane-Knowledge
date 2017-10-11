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

Go to admin/structure/media
- Press "+Add new media bundle" 
- On the **"Page?"** set the following:
  - "Lable" : "alex media bundle" // or what ever you want to call it
  - "Description" : "alex media bundle test" // or how ever you want to describe it
  - "Type provider" : "Image" // based on the meida types supported
  - "Field with source information" : "Image"  // unable to set until the image field is set later
  - "Whether to gather exif data" : "No"
  - "File MIME" : "- Skip field -"
  - "Width" : "- Skip field -"
  - "Height" : "- Skip field -"
  - "Publishing options" : "Published"
  - "Press" : "Save Media Bundle"

Go to admin/structure/media
- Open media bundle created above
- Go to the "Manage Fields" Tab and set the following fields:
  - "Press" : "+ Add field" 
  - set "Re-Use and existing field" to "Image: field_image"  // or what ever image field you are using
  - "Label" : "image"  // or what ever you want to call it
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
- Go to the "Edit" Tab and set the following fields:
  - ensure Field with source information is set to the "Image" field and defined above
  - Press "Save Media Bundle"

## Create a New Entity Browser
- Go to config/content/entity_browser
- Press "+ Add Entity browser" 
- On the "General information" page set the following fields:
  - "Label" : "Asset Browers" // or what ever you want to call it
  - Set "Display plugin" to "iFrame" //This creates an iFrame form on your page
  - Set "Widget selector plugin" to "Tabs" //the form presents options 
  - Set "Selection display plugin" to "No selectoin display"
  - Press "Next"
- On the "Display" Page set the following fields:
  - Set "Width of the iFrame" to "650"
  - Set "Height of the iFrame" to "500"
  - Set "Link text" to "Select entities"
  - Check "Auto open entity browser" box
  - Press "Next"
- On the "Widget Selector" Page set the following fields:
  - Press "Next"
- On the "Selection display" Page set the following fields:
  - Press "Next"
- On the "Widgets" Page set the following fields:
- Use the "Add widget plugin" to what widget you need  
  - "Upload" Widget
  - Adds an upload field browser's widget // adds a traditional image
  - Not very helpful
  - "View" Widget
  - "Label (View) "Your Images" 
  - "Submit button text" : "Select Images"
  - Set "View : View display" to "Entity Browser: Entity browser" View 
  - Press "Finish"
  
## Entity Browser View

## Field to attach to content
- attach new field to 
- entity reference 
  - other
  
  Type of item references
  - Media
  - Unlimited




## Create a new Image Style
- goto config/media/image-styles
- press "+ Add image style"




