[![home](./images/home.png)](./readme.md "Домой") [НА ГЛАВНУЮ](./readme.md "Вернуться на главную страницу")

<!--Можно комбинировать HTML и Markdown. / Стили в дальнейшем будем задавать в CSS, пока исп. атрибут style /-->
## Установка и настройка GIT

![logo_settings](./images/setting_icon.png)

---

### Установка

#### Windows 

Проходим по этой [ссылке](https://git-scm.com/download/win), скачиваем и устанавливаем.

В процессе установки желательно сразу указать какой редактор кода будет использовать Git по умолчанию.

#### Mac OS
~~~bash
# Если установлен Homebrew
brew install git

# Если нет, то вводим эту команду. 
git --version
# После этого появится окно, где предложит установить Command Line Tools (CLT).
# Соглашаемся и ждем установки. Вместе с CLT установиться и git
~~~

#### Linux

Открываем терминал и вводим следующую команду:

~~~bash
# Debian или Ubuntu
sudo apt install git

# CentOS
sudo yum install git
~~~

---

### Настройка

Выполните следующие команды, чтобы **Git** узнал ваше **имя** и **электронную почту**:

**git config --global user.name** <*ваше имя*> – устанавливаем **имя пользователя** (глобально);  
**git config --global user.email** <*ваш email*> - устанавливаем **email пользователя** (глобально);

#### Уровни настроек:    
  * **--system** – настройка для всех проектов ***всех пользователей***;  
  * **--global** – настройки для всех проектов ***определенного пользователя***;  
  * **--local** (*по умолчанию*) – настройки конкретного вашего ***проекта***.  

#### Еще несколько полезных команд для настройки Git:

* **git config --list** – посмотреть значения параметров конфигурации;

* **git config --list --global** – посмотреть значения параметров конфигурации ***только у текущего пользователя***;

* **git config --remove-section** <*user*>– удалить всю секцию ***user*** в настройках;

* **git config --unset** <*user.name*> – удалить определенный параметр в настройках (в данном случаем ***имя польз.***);

* **git config -h** - вывести все опции и описания команды **config**;

<!--Можно комбинировать HTML-теги и Markdown-->
По желанию можно задавать свои **алиасы** - псевдонимы для определенных команд, <u>например</u>:  
**`git config --global alias.c config`** – создать алиас для команд (**git c** вместо ~~git config~~);  
**``git config --global alias.commitall ‘!git add .; git commit’``** - создаем алиас, добавляющий все изменения текущей директории (не отслеживаемых файлов в том числе) сразу в репозиторий;

Про базовые команды в Git вы узнаете в [следующей главе](./getting_started.md "Следующая глава")

---

[![previous](./images/arrow_left.png)](./about_Git.md "Предыдущая")
пред | | след [![next](./images/arrow_right.png)](./getting_started.md "Следующая")

---

settings logo by *[ana nirwana](https://www.iconfinder.com/anir)*, 
license: *[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)*

Arrows right and left by *[Tatice](http://tatice.deviantart.com)*, 
license: *[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)*

Home icon by *[Double-J Design](http://www.doublejdesign.co.uk)*, 
license: *[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)*

Быстрый старт в Git *[Anatoly Kostrykin](https://github.com/Anatoly-web-dev)*, **2022**
