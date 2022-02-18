Инструкция для IDE PhpStorm
1) все файлы кидаем в корень проекта 
    1.2 File->Setting->Plugins проверяем установлен ли Docker
2) FIle docker-compose.yml заменяем people на наши имена которые хотим использовать -> yourNAme
    app
    2.1 container_name
    db
    2.2 container_name
    nginx
    2.3 container_name
3) File .env 
    3.1 DB_HOST = db
    3.2 DB_USERNAME= придумать (только не root)
    3.3 DB_PASSWORD= придумать (только не root) 
4) запустить docker-compose up -d 
    4.1 использовать эту команду всегди при запуске докера
    4.2 Отключить докер docker-compose down
5) alt 8 -> находим Docker -> заходим -> app, db, nbinx их цвет должен быть синим
6) заходим в app  и нажимаем правой кнопкой миши по yourNAme-app и Create Terminal
Доступ к Bash терминалу можно также получить через команду docker-compose exec app Bash
7) пишем миграцию php artisan migrate
8) настраиваем БД под новые данные в IDE и WorkBench

Ситуация когда нету розрешений  sudo chmod -R 777 /path/to/directory/with/permission