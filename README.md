 # IOTProject

# Цель:

      Цель работы - научиться работать с микрокомпьютером и разработать систему управления объектами.
      
# Задача:
      
      Задача состоит в том, чтобы управлять микрокомпьютером и включать и выключать лампу.
# Что мы хотели сделать?
      
      В начале мы подключаем все необходимые соединения, такие как мышь, клавиатура, экран, 
      и подключаем диод к компьютеру, используя два соединения в порт 39 и 40, как 
      показано на рисунке, и не перепутать +/-.

<img src="image.jpeg" width="100">

      Затем входим в систему через команду.
      sudo -i
      Затем ставим пароль
      "orangepi"
      Затем создаем рабочий порт через команду.
      
      echo 199 > /sys/class/gpio/export  // Это создаст экземпляр GPIO199.
      echo out > /sys/class/gpio/gpio199/direction // Это установит GPIO199 как ВЫХОД.
      echo 1 > /sys/class/gpio/gpio199/value  // Это установит GPIO199 HIGH.
      echo 0 > /sys/class/gpio/gpio199/value   // Это установит низкий уровень GPIO199.
