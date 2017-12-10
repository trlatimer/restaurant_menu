# Readme File for Restaurant Menu Web Application

The purpose of this project was to apply information learned through Full Stack Web Developer nanodegree through Udacity. This project involves a list of fictional restaurants and their menus. Users are first met with a page that displays a list of all of the restaurants contained in the program. The user then has the option to view the menu for each restaurant, add, edit, or delete a restaurant. Authentication and Authorization are currently in development. When viewing the menu of a restaurant, a user will see the name of each item, its price, and a description. The user also has the option to add, edit, or delete any restaurant menu item. Users can also obtain API data from the program by entering certain routes in the browser.

The database involved in this program is a mock SQLAlchemy database of fictional restaurants and their menus. The database contains the following table structures:
- restaurant
    - name
    - id
- menu_item
    - name
    - id
    - course
    - description
    - price
    - restaurant_id
    - restaurant

## REQUIRED PROGRAMS/LIBRARIES:
 1. Python
 2. Vagrant
 3. VirtualMachine
 4. Flask
 5. SQLAlchemy
 6. database_setup
 
## TO START PROGRAM:
 1. Download project files and unzip them into a directory
 2. From a Linux like terminal (ex. Git Bash, Mac Terminal, etc), navigate to where you stored this repository
 3. Ensure that the directory contains a vagrant, database_setup.py, and lotsofmenus.py files.
 4. Start vagrant by typing vagrant up and hitting enter
 - It may be necessary to type vagrant init first
 - Wait for vagrant up to complete
 5. Type vagrant ssh
 - No log in information should be needed and VM should load
 - Wait for vagrant ssh to complete
 5. cd into /vagrant and then the directory you stored the files you downloaded 
 6. Run python database_setup.py to create the database structure for the project
 7. Run python lotsofmenus.py to add data to the database
 8. Run python finalproject.py to start the program
 - The console will advise that the program has been launched on localhost:5000
 9. Open browser to localhost:5000 to view the program
 10. The first page will contain all of the restaurants within the database
 11. Navigate through the program to view, add, edit, and delete restaurants and menu items
 12. Type ^C to shutdown the program


## TO VIEW JSON API:
- Ensure the program is running and you have the website open in your browser
- Append any one of the below routes to the end of 'localhost:5000' to view the JSON API
- If a route contains '<int: restaurant_id>' replace with the id for the restaurant you wish to view
- If a route contains '<int: menu_id>' replace with the id of the menu item you wish to view
    - '/restaurants/JSON' - JSON API for the restaurants
    - '/restaurants/<int:restaurant_id>/menu/JSON' to view the JSON API for a menu within a restaurant
    - '/restaurants/<int:restaurant_id>/<int:menu_id>/JSON' to view the JSON API for a specific menu item
    
 
