ACCESS PROJECT_FRONT DO NOT ACCESS WEEK 3

Project_front is all the contents of week three with CSS applied. It’s the more complete package.

Inside the week 3 folder there are a lot of php webpages. Here are what each of them do.

Index.php is the homepage and it’s where people login or create an account. This webpage submits the username and the password to either save_user.php or loginprocess.php.

Save_user.php checks if the user exists within the database when user is creating a new account. If it does (which means the username is taken), it tells the user to go back to the login and pick a new username. If the username doesn’t exist, it generates a unique 5-digit user ID number and submits the username, user ID, and the password to the user’s database. 

Loginprocess.php checks if the username exists (when they’re logging in). If the username exists, but password doesn’t match, then it tells the user that the password/username doesn’t match and redirects to login screen. If the username exists and password matches, welcomes to the page and gives the option to go make a new outfit or view all current outfits.

Model.php gives the user the option to choose skin color and gender. This data is submitted to chooseclothes.php.

Chooseclothes.php accepts the data from model.php and changes the images to match the gender and the skin color submitted previously. It displays all the possible outfit combinations.

Choosecolor.php takes the skin, gender, top and bottom clothing chosen previously. Using a photoshop-like color picker dynamically adjusts color of both top and bottom. Tells you what specific color and hue each item is. Also provides the option to Google for the exact item for customers who want to buy their clothing online. The final option is to save the outfit into the database which takes you to the next php file.

Outfit_modifier.php takes all the data from the previous pages and submits to database. Gives user option to view all outfits or create new model.

View.php is where the user is given the option to view all of their outfits or outfits by season, a previous parameter chosen on the choosecolor.php page.

MVC API folder:

Inside week 3 there’s a folder named MVC that holds all of our API code. 

This helps developer of the site access all of the information inside the database without having to go to phpmyadmin.com. This is because that website, while hosting all of the SQL data, often has negatively impacted loading speed and has sessions that constantly time-out while unattended.

Link to mvc folder can only be accessed if user admin logs on. Inside this folder: index.php displays all the database tables.
Inside the model folder, model.php creates a model which connects to the database and to outfit.php and user.php to create a php array of the database content. Both outfit.php and user.php have a method for construction and array-building to turn the respective SQL databases into something consumable by a human.

Inside view folder, outfitlist.php and userlist.php handle the data for actually building the headers of the table that end up being displayed on index.php.

Inside controller folder, controller.php acts as a bridge between the contents in the model folder and the view folder. Index invokes the controller, controller invokes model.php, outfit.php and user.php. 
