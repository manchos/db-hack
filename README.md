[Репозиторий электронного дневника](https://github.com/devmanorg/e-diary)

## Как пользоваться
Переместите файл schoolkid_script.py в корневую директорию проекта Django, рядом с manage.py.
Далее запуститите скрипт из командной строки с имеющимися подкомандами:

```bash
python schoolkid_script.py --help
usage: schoolkid_script.py [-h] {new-comm,rm-chast,fix-marks} ...

The hack script for repo: https://github.com/devmanorg/e-diary

optional arguments:
  -h, --help            show this help message and exit

subcommands:
  valid subcommands

  {new-comm,rm-chast,fix-marks}
                        function description
    new-comm            create commendation
    rm-chast            remove chastisements
    fix-marks           remove bad marks and replace them by 5

>>>
```
## Подкоманда `new-comm`  
создает новую похвалу для указанного по имени (-kname) ученика. 
Дата похвалы совпадет с датой последнего указанного по названию (-lesson) урока.
Похвала выбирается [списка](https://pedsovet.org/beta/article/30-sposobov-pohvalit-ucenika) через random.choice. 

```bash
python schoolkid_script.py new-comm --help
usage: schoolkid_script.py new-comm [-h] [-kname CHILD_NAME]
                                    [-lesson LESSON_NAME]

optional arguments:
  -h, --help           show this help message and exit
  -kname CHILD_NAME    schoolkid name
  -lesson LESSON_NAME  lesson name
```
## Подкоманда `rm-chast` 
удаляет замечания для указанного по имени (-kname) ученика.

```bash
python schoolkid_script.py rm-chast --help
usage: schoolkid_script.py rm-chast [-h] [-kname CHILD_NAME]

optional arguments:
  -h, --help         show this help message and exit
  -kname CHILD_NAME  schoolkid name

```

## Подкоманда `fix_marks` 
правит плохие оценки, двойки или тройки на пятерки для указанного по имени (-kname) ученика.

```bash
python schoolkid_script.py fix-marks --help
usage: schoolkid_script.py fix-marks [-h] [-kname CHILD_NAME]

optional arguments:
  -h, --help         show this help message and exit
  -kname CHILD_NAME  schoolkid name

```
