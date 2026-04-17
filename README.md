# 1. Установка, настройка и запуск Nginx
  - (Структуру для сайтов брал в сети)
  - Установил `nginx` и проверил что демон поднялся
  - Создал `html` страницу в `/var/www/html`
  - в файле `/etc/hosts` добавил `127.0.0.1 tms.by`
  - Создал конфигурационный файл в `/etc/nginx/sites-available/tms.by`
  - Создал симлинк `sudo ln -s /etc/nginx/sites-available/tms.by /etc/nginx/sites-enabled`
  - Проверил конфигурацию на ошибки `sudo nginx -t` 
  - Перезарядил `nginx`
  - Чтоб положить веб-сервер нужно удалить симлинк из `/etc/nginx/sites-enabled`
  - Положил веб-сервер

 <img width="992" height="487" alt="image" src="https://github.com/user-attachments/assets/dc25f87f-fabd-40f6-885d-f8276b010d00" />

 <img width="1103" height="740" alt="image" src="https://github.com/user-attachments/assets/aefe4382-4c76-4835-b9ad-62607f92b8ad" />

 <img width="1103" height="574" alt="image" src="https://github.com/user-attachments/assets/f85a7f27-4622-4d90-8a42-37076890e15d" />

# 2. Установка, настройка apache и запуск их вместе с nginx(проксирование)
  - Установил `apache2` и проверил что демон поднялся
  - Сразу чтоб избежать конфликтов на портах `/etc/apache2/ports.conf в listed перекинул апач на 127.0.0.1:8080`
  - Написал конфиг в апаче в `sites-available`
  - Активировал `a2ensite` и декативировал дефолтный `a2dissite`, перезарядил апач
  - Переписал конфиг nginx под проксирование
  - Создал симлинк `nginx`, проверил синтаксис
  - Перезарядил оба демона и проверил их статус
  - Курл, вход на сайте через браузер, добавил логи.

<img width="1088" height="439" alt="image" src="https://github.com/user-attachments/assets/1b5099cd-b0eb-48b1-8898-e57b38d0afde" />

<img width="1088" height="756" alt="image" src="https://github.com/user-attachments/assets/9867e740-1191-42b7-a4ea-4079300ea921" />

<img width="1088" height="756" alt="image" src="https://github.com/user-attachments/assets/54812097-6e09-4760-800a-56afecf1578c" />

