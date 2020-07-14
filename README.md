# Reverse Engineering Code

In the `Develop` folder, there is starter code for a project. Begin inspecting the code to get an understanding of each file's responsibility. Then, in a Google Doc, write a tutorial explaining *every* file and its purpose. If one file is dependant on other files, be sure to let the user know.

Following the `common templates for user stories`

```
.
├── config
│   ├── middleware
│   │   └── isAuthenticated.js
│   ├── config.json
│   └── passport.js
│   
├── models
│   ├── index.js
│   └── user.js
│
├── public
│    ├── js
│    │    └── login.js
│    │    └── members.js
│    │    └── signup.js
│    ├── stylesheet
│    │    └── style.css
│    ├── login.html
│    ├── members.html
│    └── signup.html
│
├── routes
│   ├── api-routes.js
│   └── html-routes.js
│
├── package.json
└── server.js

```

# `Develop/`

### `/config/isAuthenticated.js`

* This is middleware for restricting routes a user is not allowed to visit if not logged in;
*  On line `4 - 6`, if the user is logged in, continue with the request to the restricted route
* On line `8`, if the user isn't logged in, redirect them to the login page

### `config.json`

* Alloy uses the config.json file, located in the project's app directory, to specify global values, conditional environment and platform values, and widget dependencies.


### `passaport.js`

* Passport's sole purpose is to authenticate requests, which it does through an extensible set of plugins known as strategies. 
* Line `7 - 35`, the code Tells passport we want to use a Local Strategy. In other words, we want login with a username/email and password. 
* on line `8` our user will sign in using an email, rather than a "username",
* The call back function on line `44` when a user tries to sign in this code runs
* If there's no user with the given email th the if stetmen, but the password the user gives us is incorrect
on line `25`;
* On line `31` if none of code it's above, return the user
* On line `48` we export our configured passport.

# `Develop/models/`

### index.js
* 
