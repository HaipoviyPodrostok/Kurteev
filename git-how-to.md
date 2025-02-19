Установка Git
Linux (Debian/Ubuntu):
bash
Copy
sudo apt update
sudo apt install git
Linux (Arch/Manjaro):
bash
Copy
sudo pacman -S git
macOS:
Установите через Homebrew:

bash
Copy
brew install git
Windows:
Скачайте установщик с официального сайта: git-scm.com.

Настройка Git
После установки настройте имя пользователя и email (это важно для подписи коммитов):

bash
Copy
git config --global user.name "Ваше Имя"
git config --global user.email "ваш@email.com"
Проверьте настройки:

bash
Copy
git config --list
Основные команды Git
1. Создание репозитория
Инициализация нового репозитория в текущей папке:

bash
Copy
git init
Клонирование существующего репозитория:

bash
Copy
git clone <URL-репозитория>
Пример:

bash
Copy
git clone https://github.com/username/repository.git
2. Просмотр состояния репозитория
Проверка состояния файлов:

bash
Copy
git status
Просмотр изменений в файлах:

bash
Copy
git diff
3. Добавление файлов в индекс (staging area)
Добавить конкретный файл:

bash
Copy
git add <имя_файла>
Добавить все измененные файлы:

bash
Copy
git add .
4. Создание коммита
Создать коммит с сообщением:

bash
Copy
git commit -m "Ваше сообщение о коммите"
5. Просмотр истории коммитов
Показать историю коммитов:

bash
Copy
git log
Компактный вывод:

bash
Copy
git log --oneline
6. Работа с ветками
Создать новую ветку:

bash
Copy
git branch <имя_ветки>
Переключиться на ветку:

bash
Copy
git checkout <имя_ветки>
Создать и переключиться на новую ветку:

bash
Copy
git checkout -b <имя_ветки>
Удалить ветку:

bash
Copy
git branch -d <имя_ветки>
7. Слияние веток
Переключитесь на ветку, в которую хотите влить изменения, и выполните:

bash
Copy
git merge <имя_ветки>
8. Работа с удаленным репозиторием
Добавить удаленный репозиторий:

bash
Copy
git remote add origin <URL-репозитория>
Отправить изменения в удаленный репозиторий:

bash
Copy
git push origin <имя_ветки>
Загрузить изменения из удаленного репозитория:

bash
Copy
git pull origin <имя_ветки>
Просмотр удаленных репозиториев:

bash
Copy
git remote -v
9. Отмена изменений
Отменить изменения в файле (до добавления в индекс):

bash
Copy
git restore <имя_файла>
Убрать файл из индекса (staging area):

bash
Copy
git restore --staged <имя_файла>
Отменить последний коммит (создаст новый коммит с отменой изменений):

bash
Copy
git revert HEAD
10. Игнорирование файлов
Создайте файл .gitignore в корне репозитория и добавьте туда шаблоны файлов или папок, которые Git должен игнорировать. Например:

Copy
# Игнорировать все .log файлы
*.log

# Игнорировать папку build/
build/
11. Работа с тегами
