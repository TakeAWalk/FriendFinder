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

The home and survey html pages provide links to /api/friends endpoint that returns a JSON representation of the friends that have completed the survey. Additionally, the survey provides users with a 10 question survey to contrast personalities. On submit, the profile is compared to all other friends in the database and a "best friend" based on compatibility is returned.

#### routing - apiRoutes.js & htmlRoutes.js

The apiRoutes defines the endpoint /api/friends which accepts both GET and POST requests.

- The GET request return the friends array as a JSON which contains all friends who have filled out the survey.

- The POST request takes a completed survey, formats it and determines the "best friend" by comparing the profiles scores against all friends in the database.

The htmlRoutes direct the user to the survey page when /survey is requested, otherwise a default route is set to send the user to the homepage.

#### server.js

server.js sets up the express server, gathers routes and starts the server.

### How to use the app?

#### home.html

![Homepage](https://takeawalk.github.io/FriendFinder/screenshots/homepage.PNG)

- The primary option here is to 'Go to Survey'. Alternatively you can use the links below to hit the endpoint and get a JSON representation of the friends currently in the database ![JSON of Friends](https://takeawalk.github.io/FriendFinder/screenshots/get-endpoint.PNG)
- or navigate to the GitHub repo.

#### survey.html

![Survey](https://takeawalk.github.io/FriendFinder/screenshots/survey.PNG)

Complete the survey by filling out your name, providing a url to a photo of yourself and by answering all 10 questions. Once complete, submit the information.

![Submitted Survey](https://takeawalk.github.io/FriendFinder/screenshots/onsubmit.PNG)

You now know who your "best friend" is.

## How do I use this?

- Navigate to: https://gentle-tundra-89747.herokuapp.com/

## Built Using

- [NodeJS](https://nodejs.org/en/)
- Node Packages
  - [express](https://www.npmjs.com/package/express)
  - [path](https://www.npmjs.com/package/path)
  - [body-parser](https://www.npmjs.com/package/body-parser)

## Author

David Pham - email@davidpham.ca
