#### Во время обычного аудита безопасности команда выявила проблему на сервере приложений. В коде веб-сайта был обнаружен вредоносный контент. Изучив проблему, они обнаружили, что зараженных файлов может быть больше. Перед очисткой они хотели бы найти все похожие файлы и скопировать их в безопасное место для дальнейшего исследования. Выполни задание согласно следующим требованиям:

#### В Сервер приложений #2 в размещении /var/www/html/wiki найди все файлы  с расширением .css.

#### Скопируй все эти файлы вместе с их родительской структурой каталогов в местоположение /wiki на том же сервере.

#### Не копируй всю директорию целиком /var/www/html/wiki, а только нужные файлы .

## Для выполния данного задания необходимо выполнить:
* Подключится к серверу SSH с паролем
   ```bash
    ssh venus@app02
    venus@app02's password:
   ``` 
* Переключится временно на пользователя root
  ```bash
    sudo -i
   ``` 
* Выполнить команду копирования в каталог /wiki, на сервере app2, всех найденных  файлов c расширением ".css" и их родительскую структуру каталогов из  директории  /var/www/html/wiki  на сервере app2
    ```bash
    find /var/www/html/wiki/ -type f -name "*.css"  -print0 | xargs -0 cp --parents --target-directory /wiki/
    ``` 
## Задание выполненно успешно
