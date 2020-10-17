# Social Network
This is ordinary social network.

# Libraries
- JDK 1.8
- Lombok 1.10.10
- Liquibase
- Spring boot 
- PostgreSQL

# How to run 

# backend

- After download, write in "application-dev.properties" url path to your database, username and password.
This needs to made how for spring.datasource properties and as well as for spring.liquibase properties   
- Write proprties for "Email service" in "application-dev.properties". It's needs for sends restore password links to users. 
I'm using for this gmail, so if you wanna used for this something else, don't forget to rewrite other properties, like  "spring.mail.host" 

# frontend

- copy the similarities of the front, which are located in "/ resources / static", into a separate folder

- in a text editor in the frontend folder src / settings / axios.js change axios.defaults.baseURL to localhost: 8084

- in the application.properties of the backend, set server.port to the value 8084 (it is necessary that the ports of the front and back are the same)

- install npm (included in nodejs) from https://nodejs.org/en/download/

- run the console from the admin (cmd for windows)

- execute 'npm start' in the frontend folder

- go to localhost: 8080 in the browser, everything should work

- (optional) If an error occurs with uninstalled webpack-dev-server run npm install -g webpack-dev-server (globally install the package) and add to environment
variables string% USERPROFILE% \ AppData \ Roaming \ npm \
    If you get npm ERR! code ELIFECYCLE execute sequentially:
    
    - npm cache clean --force
    - удалить node_modules и package-lock.json в папке фронта (rm -rf node_modules package-lock.json для линукс дистров)
    - npm install
    - npm start
    
