# **Работа с Git и GitHub**
![Это я размышляю над инструкцией](og_og_148879361322373683.jpg)
## 1. Проверка наличия установленного Git
В терминале выполнить команду `git --version`.

Если установлен, появится сообщение с версией программы.

## 2. Установка Git

Загрузить последню версию Git по ссылке https://git-scm.com/downloads и выполнить установку

## 3. Настройка Git

При первом использовании необходимо ввести две команды:
```
git config --global user.name «Ваше имя»
git config --global user.email ваша "почта@example.com"
```

## 4. Начало работы с репозиторием

Для начала работы с репозиторием его необходимо инициализировать при помощи команды `git init`

## 5. Основные команды git
### 5.1 Команда git status
Команда `git status` служит для получения информации о текущем состоянии git.
### 5.2 Команда git add
Команда `git add` служит для добавления файла или файлов к последнему коммиту.
### 5.3 Команда git commit
Для регистрации последних изменений служит команда `git commit`. Для добавления комментария к коммиту используйте эту команду с параметром -m: `git commit -m "текст комментария"`.

Для уже добавленных к списку отслеживания файлов можно использовать данную команду с параметром -a, например: `git commit -am "текст комментария"`
### 5.4 Команда git log
Для вывода списка всех изменений служит команда `git log`.

При использовании команды с параметром `--oneline` выводится сокращённый список изменений.

## 6. Работа с ветками
Ветки используются для разделения работы над разными частями проекта между участниками.

Для создания новой ветки используется команда `git branch <имя ветки>` или `git checkout -b <имя ветки>`. 

Для переключения между ветками используется команда `git checkout <имя ветки>`. 

Для слияния веток используется команда `git merge <имя ветки>`. При этом в текущую ветку добавляется информация из ветки, указанной в параметре *<имя ветки>*.

Для удаления ветки используется команда `git branch -d`. **ВНИМАНИЕ!** Удалить текущую ветку невозможно, для удаления ветки необходимо переключиться на любую другую (обычно ветка **master**).

Команда `git branch` без дополнительных параметров выводит список имеющихся в проекте веток, при этом текущая ветка выделена зелёным цветом и отмечена звёздочкой.


## 7. Работа с удалёнными репозиториями
Для работы с удалёнными репозиториями требуется регистрация на одном из сервисов удалённых репозиториев, например, https://github.com

Для создания удалённого репозитория достаточно следовать подсказкам сайта github.

Для создания копии внешнего репозитория на локальной рабочей станции служит команда `git clone <адрес репозитория>`.

Для синхронизации локального репозитория с удалённым используется команда `git pull`. Данная команда скачивает данные с удалённого репозитория и выполняет команду *`merge`*.

Для отправки данных с локального репозитория на удалённый используется команда `git push`. 

Для добавления своего кода в чужой проект выполняем следующие действия:
* Копируем исходный репозиторий на свой аккаунт (делаем **fork**)
* Выполняем команду `git clone` для получившейся копии репозитория
* Создаём новую ветку и в ней вносим изменения в коде
* Делаем коммиты
* Выполняем команду `git push`
* Предлагаем свои изменения при помощи кнопки **pull request** на сайте github.
