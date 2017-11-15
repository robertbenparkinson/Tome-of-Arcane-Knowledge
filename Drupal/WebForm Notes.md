# Drupal 8 Webform Notes

## options available 

Look in modules/webform/config/install for various options available 

```yml

name_of_example_element:
  '#type': select                           ##  the 'select' type is the basic dropdown select element 
  '#title': 'tile of country element'       ##  Title of the element
  '#options': country_names                 ##  Uses the 'country_names' options 
  '#title_display': before                  ##  places the title of the element before the dropdown select element

```
## basic webform element template

```yml

  '#type': 
  '#title': 
  '#description': 
  '#open': 
         
      '#type':
      '#title':
      '#title_display':
      '#options':
      
      '#default_value': 
      '#empty_option': 
      '#empty_value': 
      '#states':
        visible:
          ':input[name=""]':
            value: 
```
## Add basic markup you the form

```yml
'#markup': '<p>My Butt</p>'

```



