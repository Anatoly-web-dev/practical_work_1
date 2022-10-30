[![home](./images/home.png)](./readme.md "Домой") [НА ГЛАВНУЮ](./readme.md "Вернуться на главную страницу")

## Сравнение веток, коммитов и не только

![find_differences_logo](./images/find_differences_icon.png)

---

Сравнение в Git — это функция, анализирующая два входных набора данных и отображающая различия между ними. 

**git diff** - многоцелевая команда для сравнения коммитов, веток, файлов и т.д.

`git diff <исходная_ветка> <целевая_ветка>` - просмотреть ***изменения относительно двух веток***;

`git diff <хэш коммита>` - если указать только один ***<хэш коммита>***, то произойдет 
***сравнение рабочей директории с репозторием*** (на момент этого коммита);

`git diff (без указания веток и коммитов)` -  произойдет ***сравнение рабочей директории с индексом***; 
при этом игнорируются не отслеживаемые файлы;

Путь можно добавлять к любой форме `git diff`. Например:

~~~bash
git diff <'имя_ветки1'> <'имя_ветки2'> index.html # - сравнит ветки только по указанному файлу
~~~

`git diff --cached` - выведет ***сравнение индекса с репозиторием***. Можно указать определенный ***<хэш коммита>*** 
(*по умолчанию - текущий HEAD*)

`git diff <имя_файла или директории>` - выведутся только изменения в указанном файле или папке 
(*можно указать несколько файлов через пробел*);

`git diff --no-index <имя_файла_1> <имя_файла_2>` - сравнит между собой любые файлы на диске;

Зачастую вместе с командой `git diff` используются `git status` и `git log` для анализа текущего состояния репозитория.

---

[![previous](./images/arrow_left.png)](./history_commits.md "Предыдущая")
пред | | след [![next](./images/arrow_right.png)](./undo_changes.md "Следующая")

---

find logo by *[Bytedance Inc.](https://www.bytedance.com/en/)*, 
license: *[Apache 2.0](https://creativecommons.org/licenses/by/4.0/)*

Arrows right and left by *[Tatice](http://tatice.deviantart.com)*, 
license: *[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)*

Home icon by *[Double-J Design](http://www.doublejdesign.co.uk)*, 
license: *[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)*

LICENSE: *[MIT](./license.md "Лицензия")*