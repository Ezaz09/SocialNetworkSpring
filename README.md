# Social Network
This is ordinary social network.

# Libraries
- backend
    - JDK 1.8
    - Lombok 1.10.10
    - Liquibase
    - Spring boot 
    - PostgreSQL
- frontend 
    - Vue.js
    
# How to run 

# backend

- After a download, write in "application-dev.properties" url path to your database, username and password.
This needs to made how for spring.datasource properties and as well as for spring.liquibase properties.  
 
- Write properties for "Email service" in "application-dev.properties". It's needs for sends restore password links to users. 
I'm using for this gmail, so if you wanna used for this something else, don't forget to rewrite other properties, like  "spring.mail.host". 

# frontend

- in a text editor in the frontend folder resources / static / src / settings / axios.js change axios.defaults.baseURL to localhost: 8086

- in the application.properties of the backend, set server.port to the value 8086 (it is necessary that the ports of the front and back are the same)

- install npm (included in nodejs) from https://nodejs.org/en/download/

- run the console from the admin (cmd for windows)

- execute 'npm start' in the frontend folder

- go to localhost: 8080 in the browser, everything should work

- (optional) If an error occurs with uninstalled webpack-dev-server run npm install -g webpack-dev-server (globally install the package) and add to environment
variables string% USERPROFILE% \ AppData \ Roaming \ npm \
    If you get npm ERR! code ELIFECYCLE execute sequentially:
    
    - npm cache clean --force
    - delete node_modules and package-lock.json in a folder of frontend (rm -rf node_modules package-lock.json for linux)
    - npm install
    - npm start
    
