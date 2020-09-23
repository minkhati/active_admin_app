# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* install activeadmin and devise using bundle add instead of including gem file
`bundle add activeadmin`
`bundle add devise`
`rails g active_admin:install` 
`rails db:migrate`
* Before creating any resources migrate the active_admin database
* Create any model and then migrate the database before generating resources
`rails g model Subject name`
`rails db:migrate`
* Then create a resource using active_admin
`rails g active_admin:resource Subject`
* Create another model for Note with
`rails g model Note title body:text subject:belongs_to`
* Then create a resource using active_admin for Note
`rails g active_admin:resource note`
`rails db:migrate`
* If you want to add the resources you have generated using active_admin then you have to permit 
* different attributes of the model like you in the controller but here you have to permit those attributes 
* under the admin folder and model name
* for example for the case of Subject model
`permit_params :name, note_ids: []`
* For the custom Note field body we are using WYSIWYG Editor i.e. ActiveAdmin Quill Editor. So include activeadmin_quill_editor gem in the gemfile by using bundle add 
`bundle add activeadmin_quill_editor`


