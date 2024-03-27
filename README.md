Всі нведені команди наведені для використання у PowerShell

Steps to Reproduce

1.Створіть в своєму середовищі новий каталог з назвою "new-project".

New-Item -ItemType Directory -Path "C:\Path\To\Your\Folder\new-project"

2.Перейдіть до каталогу "new-project".

cd C:\Path\To\Your\Folder\new-project

3.Ініціалізуйте новий публічний Git-репозиторій всередині каталогу "new-project".

git init
git config --global user.name "Your Name"
git config --global user.email "your_email@example.com"


4.Створіть новий файл з назвою "README.md" і додайте до нього початковий текст.

New-Item README.md -type file

5.Підготуйте файл "README.md" до коміту.

git add README.md
git add .

Рекомендується перевірити статус змін і що буде закомічено:

git status

6.Закомітьте зміни у репозиторій з коміт повідомленням “init”.

git commit -m "init"

7.Створіть нову гілку з назвою "development" і перейдіть до неї.

git checkout -b development

8.Додайте інструкцію до файлу "README.md" і підготуйте їх до коміту.

Відкриваємо текстовий редактор і додаємо інструкцію

notepad README.md 

9.Закомітьте зміни у гілці "development" з повідомленням про коміт.

git add README.md
git add .

Рекомендується перевірити статус змін і що буде закомічено:

git status

git commit -m "Added README.md"

10.Об'єднайте зміни з гілки "development" у гілку "main".

Перейдіть у гілку main:

git checkout main

Та виконайте merge:

git merge development

11.Перевірте статус, переконайтеся, що все актуально.

git status

12.Закомітьте зміни

Якщо зміни необхідні, то відкриваємо файл и робимо їх і виконуємо коміт:

notepad README.md

git add README.md

git add . 

git commit -m "Merged development to main with changes"

git remote add origin https://github.com/your_git_name/RepositoryName.git

git branch -M main

git push -u origin main
