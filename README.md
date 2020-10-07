Social Network
Инструкция для поднятия frontend части
#frontend #instruction
1. скопировать сходники фронта, которые находятся в "/resources/static", в отдельную папку
3. в текстовом редакторе в папке фронтенда src/settings/axios.js изменить axios.defaults.baseURL на localhost:8084
4. в application.properties бэкенда выставить server.port в значение 8084 (надо чтобы порты фронта и бэка совпадали)
5. установить npm (входит в nodejs) со страницы https://nodejs.org/en/download/
6. запустить консоль от админа (cmd for windows) 
7. выполнить 'npm start' в папке фронтенда
8. зайти в браузере на localhost:8080, все должно работать
9. (опционально) Если возникнет ошибка с неустановленным webpack-dev-server выполнить npm install -g webpack-dev-server (глобально установит пакет) и добавить в environment variables строку %USERPROFILE%\AppData\Roaming\npm\
    Если возникнет ошибка npm ERR! code ELIFECYCLE выполнить последовательно:
    a) npm cache clean --force
    b) удалить node_modules и package-lock.json в папке фронта (rm -rf node_modules package-lock.json для линукс дистров)
    c) npm install
    d) npm start
При использовании PostgreSQL 
Создать базу "snet", прописать в файле "application-dev.properties" логин и пароль пользователя. 
В слуае использования MySQL - поменять URL базы в файле "application-dev.properties".
