# Express.js Homework

## Application Name: **Friend Finder**

### https://gentle-tundra-89747.herokuapp.com/

### **App Parts**

#### friends.js

Defines the friend object with the following properties:

- name
- photo (url)
- scores

Also contains a method that takes a friend and compares their scores against its own. The smaller the score, the better a match.

#### html - home.html & survey.html

The home and survey html pages provide links to /api/friends endpoint that returns a JSON representation of the friends that have completed the survey. Additionally, the survey provides users with a 10 page survey to contrast personalities. On submit, the profile is compared to all other friends in the database and a "best friend" based on compatibility is returned.

#### routing - apiRoutes.js & htmlRoutes.js

The apiRoutes defines the endpoint /api/friends which accepts both GET and POST requests.

- The GET request return the friends array as a JSON which contains all friends who have filled out the survey.

- The POST request takes a completed survey, formats it and determines the "best friend" by comparing the profiles scores against all friends in the database.

The htmlRoutes direct the user to the survey page when /survey is requested, otherwise a default route is set to send the user to the homepage.

#### server.js

server.js setsup the express server, defines the routes and starts the server.

### How to use the app?

#### home.html

![Homepage](https://takeawalk.github.io/FriendFinder/screenshots/home.PNG)

1. Using the printed table of available products, specify an item_id to purchase.
2. Specify the quantity you wish to purchase.
   - If the item is available in the quantity you requested,
     - the purchase is made,
     - the order total displayed and
     - the database is updated.
   - Otherwise you will recieve an error message of "Insufficient quantity!"

#### bamazonManager.js

The following options are available when the app is launched:

- View Products for Sale
  - Display all inventory items
    ![Image of bamazonManager inventory](https://takeawalk.github.io/UTM/12-mysql/media/manager-inventory.png)
- View Low Inventory
  - View items with stock less than 5
    ![Image of report showing items with less than 5 in stock](https://takeawalk.github.io/UTM/12-mysql/media/manager-lowinventory.png)
- Add to Inventory
  - Replenish inventory for a specific item
    ![Image of restock functionality](https://takeawalk.github.io/UTM/12-mysql/media/manager-addinventory.png)
- Add New Product
  ![Image of add a new product functionality](https://takeawalk.github.io/UTM/12-mysql/media/manager-addnewproduct.png)

## How do I use this?

- Use Node to run this app.
  - To execute the customer purchasing app, in terminal run `node bamazonCustomer.js`
  - To execute the manager app, in terminal run `node bamazonManager.js`

## Built Using

- [NodeJS](https://nodejs.org/en/)
- Node Packages
  - [inquirer](https://www.npmjs.com/package/inquirer)
  - [mysql](https://www.npmjs.com/package/mysql)
- [MySQL](https://www.mysql.com/)
  - Database: bamazon
  - Table: products

## Author

David Pham - email@davidpham.ca
