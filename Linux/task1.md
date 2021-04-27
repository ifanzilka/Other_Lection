# Задачи
## 1. Вывести только имена файлов (без пути), на которые указывают ссылки в /etc/alternatives. Дубликаты убрать.
  
    cd /etc/alternatives
    ls -l | grep l | cut -d' ' -f 13
