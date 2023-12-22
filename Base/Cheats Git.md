#dev #git #github #cheatsheet
# Git and GitHub 
 
## GIT

Выводит версию git
> git --version

### Initialization

Инициализирует пустой git репозиторий
> git init

Файл, содержащий список файлов и папок, которые git должен игнорировать при коммите
> .gitignore file

Показывает состояние файлов в рабочей директории и индексе
> git status

### Adding files to git

Добавляет файл(ы) в индекс для последующего коммита
> git add {file}

Добавляет все измененные файлы в индекс
> git add --all
> git add .

### Save changes in file

Создает коммит с заданным сообщением
> git commit -m "{message}" 

### Working with branches

Показывает список всех веток в репозитории
> git branch

Создает новую ветку с указанным именем
> git branch {branch}

Переключается на указанную ветку
> git checkout {branch}

Удаляет указанную ветку
> git branch -D {branch}

Создает новую ветку и переключается на нее
> git checkout -b {branch}

Объединяет указанную ветку с текущей веткой
> git merge {branch}

---

## GITHUB: 

### GitHub Account
Задает глобальное имя пользователя
> git config --global user.name {name}

Задает глобальный email пользователя
> git config --global user.email {email}

Добавляет удаленный репозиторий с указанным URL
> git remote add origin {URL}

Загружает все коммиты из текущей ветки в удаленный репозиторий (master branch)
> git push -u origin master

Загружает все коммиты из текущей ветки в удаленный репозиторий (current branch)
> git push

Клонирует удаленный репозиторий в локальную директорию
> git clone {URL}

Получает все изменения из удаленного репозитория и автоматически объединяет их с локальными изменениями
> git pull
