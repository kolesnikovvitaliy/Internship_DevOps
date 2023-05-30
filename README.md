# В этом репозитории я документирую, выполнение заданий на стажировке:

### IT-Инфраструктура организации:
<img align="right" src="https://github.com/kolesnikovvitaliy/Internship_DevOps/blob/main/img/infrastructure.png" width="800"/>

## Примеры выполненных работ:
### Условия заданий размещены в каталогах:
## "linux"
* Команда_find
    * Выполнить команду копирования в каталог /wiki, на сервере app2, всех найденных  файлов c расширением ".css" и их родительскую структуру каталогов из  директории  /var/www/html/wiki  на сервере app2
    ```bash
    find /var/www/html/wiki/ -type f -name "*.css"  -print0 | xargs -0 cp --parents --target-directory /wiki/
    ``` 


