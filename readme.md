## Навигация по каталогам

**cd /.** – Переход в основной каталог
**cd** – Переход в домашний каталог (переменная $HOME)
**cd /root** – Переход в каталог /root
**cd ..** – Переход на один уровень ниже
**cd /root/.ssh** – Переход в скрытую папку .ssh


## Работа с файлами

**ls -al** – Показывает файлы и каталоги в текущей папке
**pwd – Отображает** текущий рабочий каталог
**mkdir NewFolder** – Создает новый каталог с именем “NewFolder”.
**rm NewFile** – Удаляет файл с именем “NewFile”
**rm -f NewFile** – Принудительное удаление файла с именем “NewFile”
**rm -r NewFolder** – Рекурсивно удаляет каталог с именем “NewFolder”
**rm -rf NewFolder** – Принудительное удаление каталога с именем “NewFolder” рекурсивно
**cp oldfile1 newfile2** – Копирует содержимое oldfile1 в newfile2
**cp -r olddir1 newdir2** – Рекурсивно копирует каталог “olddir1” в “newdir2”. Dir2 будет создан, если он не существует.
**mv oldfile1 newfile2** – Переименовывает “oldfile1” в “newfile2”.
**ln -s /etc/log/file logfile** – Создает ярлык на файл
**touch newfile** – Создает пустой файл с именем newfile
**cat > newfile** – Помещает STDIN в newfile
**more newfile** – Выводит содержимое newfile по частям
**head newfile** – Выводит первые 10 строк файла newfile
**tail newfile** – Вывод последних 10 строк newfile
**gpg -c newfile** – Шифрует newfile в формат gpg с помощью пароля и сохраняет его в том же каталоге.
**gpg newfile.gpg** – Расшифровывает gpg файл
**wc newfile** – Выводит количество байт, слов и строк нового файла.


## Права доступа к файлам/каталогам

**chmod 777 /root/ssh** – устанавливает права rwx(чтение, запись, выполнение) на файл ssh для всех, кто имеет доступ к серверу (владелец, группа, другие)
**chmod 755 /root/ssh** – Настраивает разрешения rwx для владельца и r_x для группы и других.
**chmod 766 /root/ssh** – Устанавливает права rwx для владельца и rw для группы и других.
**chown newuser newfile** – Меняет владельца newfile на newuser
**chown newuser:newgroup newfile** – Изменяет владельца и группу-владельца для newfile на newuser и newgroup
**chown newuser:newgroup newfolder** – Меняет владельца и группу-владельца каталога newfolder на newuser и newgroup
**stat -c “%U %G” newfile** – отображает владельцев пользователей и групп newfile


## Поиск

**grep searchargument newfile** – Поиск аргумента searchargument в newfile
**grep -r searchargument newfolder** – рекурсивно просматривает все файлы в папке newfolder на наличие поискового аргумента
**locate newfile** – Показывает все местоположения нового файла
**find /etc/ -name “searchargument”** – Находит файлы с именем, начинающимся с searchargument, в каталоге /etc
**find /etc/ -size +50000k** – Найти файлы размером более 50000k в каталоге /etc.
