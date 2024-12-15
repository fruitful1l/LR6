# LR6
Лабораторная работа №6

__Цель лабораторной работы:__ изучение базовых возможностей системы управления версиями, получение опыта работы с Git Api, опыта работы с локальным и удаленным репозиторием.

__Клонирование репозитория на компьютер__
```
lla83@DESKTOP-SVIK4RJ MINGW64 ~
$ git clone https://github.com/fruitful1l/LR6.git
Cloning into 'LR6'...
remote: Enumerating objects: 31, done.
remote: Counting objects: 100% (21/21), done.
remote: Compressing objects: 100% (19/19), done.
remote: Total 31 (delta 2), reused 20 (delta 2), pack-reused 10 (from 1)
Receiving objects: 100% (31/31), 314.90 KiB | 2.40 MiB/s, done.
Resolving deltas: 100% (2/2), done.
```
![Клонирование репозитория](./scrshts/clone.png)

__Добавление файла в репозиторий средствами GitHub__

![Добавление текстового файла](./scrshts/file.png)

__Подтягиваем изменения в локальный репозиторий__
```
lla83@DESKTOP-SVIK4RJ MINGW64 ~/Documents/GitHub/LR6 (master)
$ git pull
Already up to date.
```
![pull](./scrshts/localfile.png)

__История операций для ветки master__
```
lla83@DESKTOP-SVIK4RJ MINGW64 ~/Documents/GitHub/LR6 (master)
$ git log
commit c624130e557212d9fa68d8f68ca6cbd057afe7fb (HEAD -> master)
Merge: 6f9a60e 0f9f50d
Author: fruitful1l <lla83016steam@gmail.com>
Date:   Fri Nov 29 13:54:38 2024 +0300

    Merge branch 'branch1'

commit 6f9a60e863cfb75ea5cd7849f0233581710b5362 (origin/master, origin/HEAD)
Author: fruitful1l <lla83016steam@gmail.com>
Date:   Fri Nov 29 13:44:41 2024 +0300

    Create file.txt

commit 921f53b8d0cebf542c791cf31f04e9b792f385a4 (upstream/master, upstream/HEAD)
Author: Kurtyanik <45309985+Kurtyanik@users.noreply.github.com>
Date:   Sat Nov 21 20:09:49 2020 +0300

    Обновление информации

commit 0f9f50db68a6983b47398017545532cd0f992846 (upstream/branch1)
Author: Kurtyanik <45309985+Kurtyanik@users.noreply.github.com>
Date:   Sat Nov 21 20:08:33 2020 +0300
```
![masterlog](./scrshts/hist.png)

__Попытка слияния__

![merge](./scrshts/mergeatt.png)

__Разрешение конфликта слияния__

В процессе разрешения конфликта слияния было принято решение изменить mergefile.txt в master

![fixmerge](./scrshts/cofsol.png)

__Коммит о слиянии веток__

![mergecommit](./scrshts/mergecompl.png)

__Удаление ветки__

![branchdelete](./scrshts/branchdel.png)

__Создание ветки для отчёта__

![branchcreate](./screenshots/newbranch.png)
Лог команд:
```
git clone https://github.com/fruitful1l/LR6.git  - клонирование репозитория на компьютер
cd LR6/  - переход в папку репозитория
git pull  - подтягивание изменений
git log origin/branch1  - получение истории операций для ветки branch1
git merge branch1  - слияние с веткой branch1
git commit -m "Merged branch1"  - коммит об успешном слиянии
git branch --delete branch1  - удаление ветки branch1
mkdir scrshts - создание папки
git status  - получение статуса репозитория
git commit -m "подпись и скриншоты"  - коммит
vim the_file.txt  - изменение файла the_file.txt
git revert - откат коммита
git commit -m "reverted the_file.txt modification"  - коммит об откате коммита
git push --set-upstream origin report - создание новой ветки и переход на неё
git switch report  - переключение на ветку отчёта
```
История операций:
```
372eeec 2024-10-23 fruiful1l Отчет
ded3fc4 2024-11-29 fruiful1l Имена скриншотов
3c9e8c6 2024-11-29 fruiful1l Добавлены скриншоты
c624130 2024-10-23 fruiful1l Merged branch1
6f9a60e 2024-10-23 fruiful1l Create file.txt
921f53b 2020-11-21 GitHub Обновление информации
0f9f50d 2020-11-21 GitHub Заполнил файл
c08a654 2020-11-21 GitHub Файл создан пустым
3c6e913 2020-11-21 GitHub Initial commit
```
__Вывод:__ Я изучил базовые возможности системы управления версиями, получил опыт работы с Git Api, опыт работы с локальным и удаленным репозиторием.
