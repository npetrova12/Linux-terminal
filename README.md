# Linux-terminal
HW_1 Terminal

1) Посмотреть где я ---- pwd
2) Создать папку ---- mkdir 1
3) Зайти в папку ---- cd 1
4) Создать 3 папки ----  mkdir one two three
5) Зайти в любоую папку ----  cd one
6) Создать 5 файлов (3 txt, 2 json) ---- touch file1.txt file2.txt file3.txt file4.json file5.json
7) Создать 3 папки ---- mkdir 1 2 3
8) Вывести список содержимого папки ---- ls -la
9) Открыть любой txt файл  
a) cat >> file1.txt
b) vim q1.txt
10) написать туда что-нибудь, любой текст. 
a) Совы кричат очень громко.
b) "i" Совы кричат очень громко.
11) сохранить и выйти.  
a) ctrl+c
b) "esc", ":wq"
12) Выйти из папки на уровень выше --- cd ..
13) переместить любые 2 файла, которые вы создали, в любую другую папку.  
а) mv one/{file1.txt,file2.txt} three
б) mv one/file1.txt one/file2.txt three
14) скопировать любые 2 файла, которые вы создали, в любую другую папку.
a) cp one/{file3.txt,file4.json} two
b)cp one/file3.txt one/file4.json two
15) Найти файл по имени ---- find -name file1.txt
16) просмотреть содержимое в реальном времени (команда grep) изучите как она работает. 
a) tail -f file1.txt
b) grep громко file1.txt
Совы кричат очень громко.
c) grep -v privet file1.txt
Совы кричат очень громко. (поиск строк без слова privet)
d)grep -c privet file1.txt
0 (показывает количество строк со словом privet)
17) вывести несколько первых строк из текстового файла ---- head -2 file1.txt
18) вывести несколько последних строк из текстового файла ---- tail -2 file1.txt
19) просмотреть содержимое длинного файла (команда less) изучите как она работает. ---- less file1.txt 
20) вывести дату и время ---- date


=========

Задание *
1) Отправить http запрос на сервер.
curl "http://162.55.220.72:5005/terminal-hw-request"

curl "http://162.55.220.72:5005/get_method?name=nastya&age=30"

2) Написать скрипт который выполнит автоматически пункты 3, 4, 5, 6, 7, 8, 13
touch script.sh
cat >> script.sh
#!/bin/bash
cd part2
mkdir 1 2 3
cd 1
touch file1.txt file2.txt file3.txt file4.json file5.json
mkdir privet1 privet2 privet3
ls -la
mv file1.txt file2.txt privet1
"ctrl+c"
chmod +x ./script.sh
./script.sh
