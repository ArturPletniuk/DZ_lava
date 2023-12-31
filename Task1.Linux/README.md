# Задание 1

#### *Linux* - Выполнить в командной строке

![pictures linux for interim certification](https://raw.githubusercontent.com/Terekhov-A-S/interim_certification_java/main/Task%201.%20Linux/Linux1.jpg)

-----

0) Подключаемся по SSH к виртуальной машине

```
ssh -p 8022 testuser@localhost
вводим пароль
```
![pictures linux-0 for interim certification](https://raw.githubusercontent.com/Terekhov-A-S/interim_certification_java/main/Task%201.%20Linux/0.png)

-----

1) Используйте команды операционной системы Linux и создайте две новых директории – «Игрушки для школьников» и «Игрушки для дошколят»

```
mkdir 'Игрушки для школьников'
mkdir 'Игрушки для дошколят'
```
![pictures linux-1 for interim certification](https://raw.githubusercontent.com/Terekhov-A-S/interim_certification_java/main/Task%201.%20Linux/1.png)

-----

2) Создайте в директории «Игрушки для школьников» текстовые файлы - «Роботы», «Конструктор», «Настольные игры»

```
cd Игрушки\ для\ школьников/
touch Роботы.txt
touch Конструктор.txt
touch 'Настольные игры'.txt
```
![pictures linux-2 for interim certification](https://raw.githubusercontent.com/Terekhov-A-S/interim_certification_java/main/Task%201.%20Linux/2.png)

-----

3) Создайте в директории «Игрушки для дошколят» текстовые файлы «Мягкие игрушки», «Куклы», «Машинки»

```
cd ..
cd Игрушки\ для\ дошколят/
touch 'Мягкие игрушки'.txt
touch 'Куклы'.txt
touch 'Машинки'.txt
```
![pictures linux-3 for interim certification](https://raw.githubusercontent.com/Terekhov-A-S/interim_certification_java/main/Task%201.%20Linux/3.png)

-----

4) Объединить 2 директории в одну «Имя Игрушки»

```
cd ..
mkdir 'Имя игрушки'
cp -r /home/testuser/'Игрушки для школьников'/* /home/testuser/'Имя игрушки'
cp -r /home/testuser/'Игрушки для дошколят'/* /home/testuser/'Имя игрушки'
rm -r 'Игрушки для школьников'
rm -r 'Игрушки для дошколят'
```
![pictures linux-4 for interim certification](https://raw.githubusercontent.com/Terekhov-A-S/interim_certification_java/main/Task%201.%20Linux/4.png)

-----

5) Переименовать директорию «Имя Игрушки» в «Игрушки»

```
mv ~/'Имя игрушки' ~/Игрушки
```
![pictures linux-5 for interim certification](https://raw.githubusercontent.com/Terekhov-A-S/interim_certification_java/main/Task%201.%20Linux/5.png)

-----

6) Просмотреть содержимое каталога «Игрушки».

```
cd 'Игрушки'
ls -al
```
![pictures linux-6 for interim certification](https://raw.githubusercontent.com/Terekhov-A-S/interim_certification_java/main/Task%201.%20Linux/6.png)

-----

7) Установить и удалить snap-пакет. (Любой, какой хотите)

```
snap search gimp
sudo snap install gimp
sudo snap list
sudo snap remove gimp
```
![pictures linux-7_1 for interim certification](https://raw.githubusercontent.com/Terekhov-A-S/interim_certification_java/main/Task%201.%20Linux/7_1.png)

![pictures linux-7_2 for interim certification](https://raw.githubusercontent.com/Terekhov-A-S/interim_certification_java/main/Task%201.%20Linux/7_2.png)

-----

8) Добавить произвольную задачу для выполнения каждые 3 минуты (Например, запись в текстовый файл чего-то или копирование из каталога А в каталог Б).

```
crontab -e
*/5 * * * * echo 'Очередная новая запись про очередную новую куклу' >> /home/testuser/Игрушки/Куклы.txt
```
![pictures linux-8_1 for interim certification](https://raw.githubusercontent.com/Terekhov-A-S/interim_certification_java/main/Task%201.%20Linux/8_1.png)

![pictures linux-8_2 for interim certification](https://raw.githubusercontent.com/Terekhov-A-S/interim_certification_java/main/Task%201.%20Linux/8_2.png)

-----

*Подготовил студент Geek Brains* [**`Плетнюк Артур`**](https://gb.ru/users/), interim_certification_java
