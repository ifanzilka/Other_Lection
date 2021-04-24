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
