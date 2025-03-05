# 🚀 Git Mastery Guide | Полное руководство по Git

![Git Logo](https://git-scm.com/images/logo@2x.png)  
*Для новичков и профессионалов: все команды, схемы и лайфхаки*

---

## 🛫 Быстрый старт

### 🔄 Стандартный рабочий цикл
```bash
# Добавить все изменения
git add .

# Проверить статус (рекомендуется!)
git status

# Создать коммит
git commit -m "✨ Добавил новую функциональность"

# Отправить на GitHub (после первого раза можно просто git push)
git push origin main


🆕 Первая настройка репозитория
# Инициализация
git init

# Привязка к удалённому репозиторию
git remote add origin https://github.com/ВАШ_ЛОГИН/ВАШ_РЕПОЗИТОРИЙ.git

# Первый пуш
git push -u origin main


📜 Основные команды
🗂 Навигация
Команда	Действие	Пример
pwd	Показать текущий путь	pwd
ls	Список файлов	ls -a (со скрытыми)
cd <папка>	Перейти в папку	cd projects
cd ..	На уровень выше	cd ..


📁 Работа с файлами
# Создать файл/папку
touch index.html
mkdir src

# Копирование и перемещение
cp file.txt backup/
mv old.txt new.txt

# Удаление
rm file.txt
rm -r folder/  # Рекурсивное удаление


🔄 Схема статусов файлов (Mermaid)
graph LR;
    untracked("🆕 Untracked") -- "git add" --> staged("✅ Staged");
    staged -- "git commit" --> tracked("📦 Tracked");
    tracked -- "Изменение файла" --> modified("✏️ Modified");
    modified -- "git add" --> staged;
    tracked -- "Удаление файла" --> untracked;
    
    classDef statusStyle fill:#f9f,stroke:#333,stroke-width:2px;
    class untracked,staged,tracked,modified statusStyle;


🌿 Ветвление
Основные команды
# Создать и переключиться на ветку
git checkout -b feature

# Слияние веток
git merge feature

# Удаление ветки
git branch -d feature


Визуализация истории
git log --graph --oneline --all

☁️ Работа с GitHub
Клонирование и обновление
# Скачать репозиторий
git clone https://github.com/user/repo.git

# Получить свежие изменения
git pull origin main


Решение конфликтов
# После разрешения конфликтов:
git add .
git commit -m "Merge conflict resolved"
git push



🧰 Продвинутые инструменты
🔙 Отмена изменений

# Отменить изменения в файле
git restore file.txt

# Отменить индексацию
git restore --staged file.txt

# Переписать последний коммит
git commit --amend


🕵️ История изменений
# Показать изменения в файле
git diff HEAD~1 -- file.txt

# Поиск по коммитам
git log --grep="bugfix"


🚫 Игнорирование файлов (.gitignore)
# Пример файла .gitignore
node_modules/
*.log
.DS_Store
.env
dist/

💡 Профессиональные советы
Коммиты-сообщения:
Используйте формат:
тип(область): описание
Пример: feat(auth): добавить OAuth-авторизацию

Интерактивное добавление:
git add -p  # Пошаговый выбор изменений

Шпаргалка статусов:
git status -s  # Компактный вывод

🚨 Помните:
git push --force может быть опасен!
Всегда делайте git pull перед работой с веткой!


