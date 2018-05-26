## About

Real-time file-based server for quick api testing

## Getting Started

1. Make sure you have [NodeJS](https://nodejs.org/) and [npm](https://www.npmjs.com/) installed.
2. Install your dependencies

    ```
    cd path/to/local-messaging; npm install
    ```

3. Start your app

    ```
    npm start
    ```

## API basics

GET & POST to /messages

e.g. curl 'http://localhost:3030/messages/' -H 'Content-Type: application/json' --data-binary '{ "name": "Me", "text": "Hello from the command line!" }'

Update 

    src/services/messages/messages.hooks.js
    
to lock messages from unauthorised users


Authorise via POST to /authentication

    curl 'http://localhost:3030/authentication/' -H 'Content-Type: application/json' --data-binary '{ "strategy": "local", "email": "feathers@example.com", "password": "secret" }'

Add users via POST to /users

    curl 'http://localhost:3030/users/' -H 'Content-Type: application/json' --data-binary '{ "email": "loginName", "password": "passwd" }'
    
