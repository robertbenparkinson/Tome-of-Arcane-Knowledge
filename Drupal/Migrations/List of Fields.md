#List of Drupal 8 Migration Fields 

##Plugins

###entity:user

```yml
  destination:
      plugin: entity:user
  process:
      uid:  
      name: name            ##user name
      pass: password        ##password
      mail: email           ##email
      status:               ##active or blocked 0/1
      created:              ##the time the account was created
      access:               ##first accessed
      login:                ##last time they logged it
      roles:                ##user roles
      role_names:           ##
      picture:
      signature
      signature_format
      timezone
      language:             ##users language "en" "it", etc
      init
      data
      is_new

```
