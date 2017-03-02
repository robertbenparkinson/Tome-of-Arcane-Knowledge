#List of Drupal 8 Migration Fields 

##Plugins

###entity:user

```yml
  destination:
      plugin: entity:user
  process:
      ##uid:  user_id       ##user id              
      name: name            ##username
      pass: password        ##password
      mail: email           ##email
      status:               ##active or blocked active =1 blocked = 0 , 0/1
      created:              ##the time the account was created
      access:               ##first accessed
      login:                ##last time they logged it
      changed:              ##last updated?
      roles:                ##user roles
      role_names:           ##
      picture:
      signature             ##users default signature
      signature_format      ##text format "HTML", "Filtered HTML" or "Full Html"
      timezone : timezone_name
      language:             ##users language "en" "it", etc
      init                  ##email
      data                  ##misc user data
      is_new                ## D7 only 

```

### 'entity:file'

```yml

destination:
    plugin: 'entity:file'
    source_base_path: 
    source_path_property:
    urlencode: true
    destination_path_property:
    
process:
    fid: 
    filename:
    uri:
    uid:
        -
