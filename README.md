# CHAPTER 5
* Add stylesheet sass for all pages (home, help, contact, signup)
* Separate the partition of pages (head, header, footer)
* Create the test module for corresponding pages
* Assign paths/routes for each pages

# CHAPTER 6
* Create the database for Users on mysql2
* Set constraints for Users model (name, email, password (hash))
* Create test cases corresponding to new requirements, mostly the users' model authentications.

# CHAPTER 7
* Create sign-up pages, sign-up error messages,  and its functions
* Create test cases corresponding to new requirements, mostly the sign-up authentications.
* Set up production webserver 

# CHAPTER 8
* Setup missing requirements
    * Import javascript related gems
    * Import missing gems
* Create login, logout functions
* Create test cases corresponding to new requirements, mostly the log-in/logout authentications.
* Try to debug with pry gem

# CHAPTER 9
* Associate to each user a remember token and a corresponding remember digest for use in persistent sessions.
* Create ```remember_me``` checkbox to allow users to save the sessions or not. 
    * Login status is determined by the presence of a current user based on the temporary session’s user id or the permanent session’s unique remember token.
* Create integration tests which can verify correct routes, database updates, and proper changes to the layout.

# CHAPTER 10
* Users can be updated using an edit form, which sends a PATCH request to the update action.
* Safe updating through the web is enforced using strong parameters. 
* implement an authorization using before filters.
* Authorization tests use both low-level commands to submit particular HTTP requests directly to controller actions and high-level integration tests.
* Friendly forwarding redirects users where they wanted to go after logging in.
* The users index page shows all users, 30 users per page.
* Admins can delete users through the web by clicking on delete links that issue DELETE requests to the Users controller ```destroy``` action.
* Use the standard file ```db/seeds.rb``` to seed the database with sample data using ```rails db:seed```.

# CHAPTER 11
* Create the activation account function which users are required to activate before using their accounts.
    * Add ```activation_digest``` and ```activated``` to the users table
    * The link to activate account consists of the ```activation_digest``` and the email in ASCII. 
* Alter the integration tests to adapt new requirements for sign up and log in.

# CHAPTER 12
* Create the reset password function for users.
    * Add ```reset_digest```  and ```reset_sent_at``` to the users table
    * Create a ```reset_token``` which is valid in a specific span of time by checking the ```reset_sent_at```
* Create the integration tests to examine the reset password function

# CHAPTER 13
* Create Micropost model and associate it to User model
* Create functions for users to handle microposts: ```create```, ```destroy```
* Use ```where``` method to perform Active Record selections in order to get risk of SQL injection. 
* Upload and resize uploaded images with CarrierWave
