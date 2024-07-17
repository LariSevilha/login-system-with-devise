# README

Change database in gemfile from sqlite3 to pg

Change configuration database.yml for pg

Add to the Gemfile the devise gem and the devise i18n gem (translates the messages)

Use the commands:  

    1- rails generate devise:install  
    
    2- rails generate devise User  
    
    3- rails db:migrate  
    
    4- rails generate devise:views  
    
Add to the gemfile the gemfile: 

    gem 'rails_admin'
    
    gem 'cancancan'
    
    gem "sassc-rails"
    
To generate Rails Admin, use the command rails generate rails_admin:install.

After that, uncomment the lines in the rails_admin.rb file:
    
    config.authenticate_with do
    
      warden.authenticate! scope: :user
      
    end
    
    config.current_user_method(&:current_user)

* ...
