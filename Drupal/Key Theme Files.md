# Drupal Key Custom Theme Files

## ***.info.yml

```yml
name: ***
type: theme
description: 'custom theme'
core: 8.x
base theme: false

libraries:
  - ***/bootstrap
```
<b>IMPORTANT!</b>
* No Tabs!!!! yml hates them
* Watch the spaces!


## ***.libraries.yml

```yml
bootstrap:
  version: 3.3.7
  css: 
    theme:
      vendor/bootstrap/css/bootstrap.min.css: {}
      vendor/bootstrap/css/bootstrap-theme.min.css: {}
  js:
    vendor/bootstrap/js/bootstrap.min.js: {}
  dependencies:
    - core/jquery
 ```
<b>IMPORTANT!</b>
* No Tabs!!!! yml hates them
* Watch the spaces!
* Make sure the css, js and the dependencies lines all line up!!!
* Make sure all of the external libraries are in the right place. For example the bootstrap files are placed in the <b>vendor/</b> file in our theme file


