version project : 
php 5.
Structure project
    ├── Controller

│   └── Api

│       ├── BaseController.php

│       └── UserController.php

├── inc

│   ├── bootstrap.php

│   └── config.php

├── index.php

└── Model

    ├── Database.php

    └── UserModel.php

    index.php: the entry-point of our application. It will act as a front-controller of our application.
    inc/config.php: holds the configuration information of our application. Mainly, it will hold the database credentials.
    inc/bootstrap.php: used to bootstrap our application by including the necessary files.
    Model/Database.php: the database access layer which will be used to interact with the underlying MySQL database.
    Model/UserModel.php: the User model file which implements the necessary methods to interact with the users table in the MySQL database.
    Controller/Api/BaseController.php: a base controller file which holds common utility methods.
    Controller/Api/UserController.php: the User controller file which holds the necessary application code to entertain REST API calls.

Call REST API
// https://localhost/index.php/{MODULE_NAME}/{METHOD_NAME}?limit={LIMIT_VALUE}

http://localhost/index.php/user/list?limit=20
localhost/learn_restful_api/index.php/user/list?limit=20
output
[

   {

      "user_id":1,

      "username":"Bob",

      "user_email":"bob@gmail.com",

      "user_status":0

   },

   {

      "user_id":2,

      "username":"John",

      "user_email":"john@gmail.com",

      "user_status":1

   },

   {

      "user_id":3,

      "username":"Mark",

      "user_email":"mark@gmail.com",

      "user_status":1

   },

   {

      "user_id":4,

      "username":"Ville",

      "user_email":"ville@gmail.com",

      "user_status":0

   }

]
