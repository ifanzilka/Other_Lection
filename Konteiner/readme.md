# Konteiners

 proc ->  папка с содержимым процееса
  
    chroot меняем папку с файлами 


#### proc/PID/cmdline -> комнда которая запустила процесс

#### proc/PID/cwd -> ссылка на текущую дерикторию 

#### proc/PID/environ -> переменные оркужения

#### proc/PID/exe -> ссылка на оригинальный запущенный файл 

#### proc/PID/root -> ссылка накорневой каталог

#### proc/PID/status ->инофрмация о состоянии процееса 

    chroot . /bin/bash



## У Докера такая же аналогии (ограничить процесс)
  
   Запуск Контейнера
   
   
    docker run ubuntu ls


Чтобы получить stdin/stdout 

    docker run --interactive ubuntu

Чтобы подключить терминал 

    docker run --interactive --tty ubuntu


Скачиваем образ контейнера с dockerhub
   
    docker pull ubuntu
 
 Какие Докеры работают(процессы)
 
    docker ps
Делаем изменения и загружаем 

    docker commit [CONTAINER]
    docker push [...]
Заново запусукаем 

    docker restart ...
    docker attach ...
Для получения доступа к файлам внутри контейнера

     docker run --it --volume $(pwd) : /task54 ubuntu
(мы сказали чтобы папка pwd подмонтировалась в контейнер под названием /task54)

Список volume

    docker volume ls
    //Create
    docker volume create my-volume     
Используем

    docker run --it --volume my-volume : /volume ubuntu
    
Даем имя контейнеру
    
     docker run --it --name my-name --volume  $(pwd) : /task54 ubuntu
Запуск в фоне и пробрасивание портов
    
    docker run --detach --publish 8080:80 nginx
  
   (С 8080 порта ПК на 80 порт контейнера)
Удаление 

    docker rm (хэш)
