Ruby On Rails *(Incomplete)*
===

Installation
---
**Requirements**

+ Ruby, Rails, Command Line Tools

**Command Line Tools**

+ Install *Xcode* through App Store
+ Open *Xcode* and go to *Preferences...* or type `CMD+,`
+ Under the *Downloads* tab, download and install Command Line Tools

**Ruby**

+ Install RVM by opening a Terminal and typing the command:

		$ \curl -L https://get.rvm.io | bash -s stable --rails --autolibs=enabled

    *(must have Git installed to run this command)*

+ To make RVM available in Shell, need to update *.bash_profile* file:

		cd ~/
		sudo vim .bash_profile

[**Rest of Tutorial**](http://net.tutsplus.com/tutorials/ruby/how-to-install-ruby-on-a-mac/)


Initial Setup
---
+ rails new <name_of_project> # "-d mysql" to use MySQL database"


Setup MySQL Database
---
+ run mySQL server (ex: MAMP)
+ go to config/database.yml and add:
	"socket: /Applications/MAMP/tmp/mysql/mysql.sock"
	under development, test and production
	"password: root" (default password is set to root)
+ to change password, in a terminal type:
	"mysql -u root -p"
	then add a password or leave blank and press enter
	(this sets the password to access the database)

+ type: "rails s" or "rails server" to start server


**May Need to change socket path**

+ Creat a file called *my.cnf* in /etc *(cd /etc)*
+ in *my.cnf* file: add lines:

		[client]
		socket=/Applications/MAMP/tmp/mysql/mysql.sock

+ Run the following in main folder to update database:
		
		rake db:migrate

+ *to undo migrate*:

		rake db:rollback

Add Table/Data to Database
---
+ type: rails generate scaffold <TableName> <field_name>:<data_type> [,<field_name>:<data_type>...]
 to create table with fields

+ run "rake db:migrate" to add table/fields to mySQL database
 + will not migrate if table already exists
 + to add a field, need to destroy scaffold and generate a new one with the new fields
 + Field Types:
   - :primary_key, :string, :text, :integer, :float, :decimal, :datetime, :timestamp, :time, :date, :binary, :boolean




##TODO
add Links/References



#Working with Rails

####To add a new static page:

1. Go to <view>_controller.rb and add:

		def <pageName>
			#can add functions/variables here
		end

2. Create **<pageName\>.html.erb** to *app/views/<view\>/*
3. add the following code snippet to *routes.rb*:

		get "<pageName>" => "<view>#<pageName>"


####Adding Stuff to database:
when using heroku:

	heroku run rake db:migrate

update heroku:

heroku push 

####Use Devise for Log in/Sign up Accounts

(add gitHub link to Ruby Devise)

####Adding Gems

1. goto Gemfile and add
		gem '<gem name>', <gem version>


		