# Blog project using Ruby on Rails

This is the first blog project made using the rails tutorial found [here](https://guides.rubyonrails.org/getting_started.html).

This repo is being used to create a blog or similar and experiment on the rails framework.

</br></br>

# Creating Login Authentication

Execute the command lines:
```
bundle add 'devise'

bundle install

rails g devise:install
```

add `config.action_mailer.default_url_options = { host: 'localhost', port: 3000 }` to `config/environments/development.rb`

run: 
```
rails g devise:views
```

Create a user:
```
rails g devise User
```

This will generate a new migration file which will add some columns to the user table:
```
rails g migration add_name_to_users name:string surname:string
```

Execute the database migration. On your terminal, you can either do:
```
rails db:migrate
```
or 
```
rake db:migrate
```

Run the rails server and go to `http://localhost:3000/users/sign_up`



[Tutorial](https://hackernoon.com/using-devise-in-your-ruby-on-rails-application-a-step-by-step-guide-m92i3y5s)

