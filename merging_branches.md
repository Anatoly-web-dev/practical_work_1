[![home](./images/home.png)](./readme.md "Домой") [НА ГЛАВНУЮ](./readme.md "Вернуться на главную страницу")

##  Слияние веток

![git_merge_logo](./images/merge_git_icon.png)

---

В Git есть два способа внести изменения из одной ветки в другую: 
* **Слияние**
* **Перебазирование** (*разберем в [следующей главе](./rebasing.md "следующая глава")*)

В этой главе вы узнаете о слиянии веток и команде `git merge`

`git merge <название_ветки>` - все изменения из указанной ветки добавить в ветку ***master***. Есть ньюансы:  

* **!** нужно переключиться на ветку ***master*** и находиться в ней, когда выполняем ***merge***!  
* **!** Такой способ работает только с ветками, которые являются прямыми потомками вершины ветки ***master***!
(в которых нет своих собственных независимых коммитов);

Разберем подробнее, что нам выводит Git в консоли, после выполнения команды `git merge`:
~~~bash
git merge fix - # добавляется изменения из указанной ветки fix в ветку master;

Updating 5d58e96..27ae510 - # указывается что с чем сливаем (первый коммит - вершина ветки master, второй коммит - вершина указанной ветки fix);

Fast-forward - # указывается метод алгоритма при слиянии (fast-forward - самый простой, коммиты указанной ветки становятся коммитами ветки master, указатель ветки master переносится на вершину указанной ветки).
~~~

### Также могут пригодиться следующие команды

`git merge --no-ff` - выполнить коммит слияния;

`git merge --abort` - прекращение слияния при конфликте;

Отменить последний ***merge*** и вернуть предыдущую версию ветки ***master***:  
1. `cat .git/ORIG_HEAD` - посмотреть старый идентификатор ветки ***master***, который был до ***merge***;  
2. `git branch -f master ORIG_HEAD` - отменить ***merge***, вернуть предыдущую версию ветки ***master***;
3. `git checkout -B** <*master*> <*имя_ветки*>` - перенести ветку ***master*** обратно на указанную ветку;

---

[![previous](./images/arrow_left.png)](./branches_basic.md "Предыдущая")
пред | | след [![next](./images/arrow_right.png)](./rebasing.md "Следующая")

---

git merge logo by *[TeenyIcons](https://teenyicons.com/)*, 
license: *[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)*

Arrows right and left by *[Tatice](http://tatice.deviantart.com)*, 
license: *[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)*

Home icon by *[Double-J Design](http://www.doublejdesign.co.uk)*, 
license: *[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)*

Инструкция по работе с GIT  
***[Anatoly Kostrykin](https://github.com/Anatoly-web-dev)***, **2022**