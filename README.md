Запуск контейнера с backend-сервером Django
-
Ссылка на задание: https://github.com/netology-code/py-homeworks-web/tree/new/1.3-docker

Для сборки и запуска контейнера с backend-сервером, выполните следующие команды:


1. **Сборка образа из файла Dockerfile:**
 
>docker build --tag hw_crud01

    --tag собирает образ hw_crud01 из Dockerfile 

2. **Запуск контейнера:**

>docker run -d -p 8001:8000 --name hw_crud hw_crud01

    -d (--detach) запускает Docker в фоновом режиме и освобождает консоль. 

    -p (--publish) 8001:8000 перенаправляет трафик с внешнего порта 8001 на внутренний порт контейнера 8000.

    -n (--name) задает имя контейнера (hw_crud) для дальнейших манипуляций

    hw_crud01 - имя запускаемого образа

3. **Остановка запущенного контейнера:**
>docker stop hw_crud
