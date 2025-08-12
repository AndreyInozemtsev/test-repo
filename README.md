
# Руководство по базовым операциям в GitLab

## 1. Создание репозитория с .gitignore и README
1. На главной странице GitLab нажмите **"New project"**
2. Выберите **"Create blank project"**
3. Заполните:
   - Project name: `ваш-проект`
   - Выберите видимость (Private/Public)
4. В секции **"Initialize repository with"**:
   - ☑️ Добавить `.gitignore`: выберите шаблон (например, *Python*)
   - ☑️ Добавить `README.md`
5. Нажмите **"Create project"**  
![Шаг создания репозитория](screenshots/create_repo.png)

## 2. Создание веток develop и master
1. В репозитории перейдите: **Repository → Branches**
2. Нажмите **"New branch"**
3. Создайте ветки:
   - Branch name: `master` (создается автоматически)
   - Branch name: `develop` (введите вручную)  
![Создание ветки develop](screenshots/create_develop.png)

## 3. Установка develop как ветки по умолчанию
1. **Settings → Repository**
2. Раскройте **"Default branch"**
3. Выберите `develop` из выпадающего списка
4. Нажмите **"Save changes"**  
![Изменение ветки по умолчанию](screenshots/set_default_branch.png)

## 4. Создание issue
1. В меню выберите **Issues → New issue**
2. Заполните:
   - Title: `Создать мануал по GitLab`
   - Description: Детали задачи
   - Assignee: Назначьте себя
3. Нажмите **"Create issue"**  
![Создание issue](screenshots/create_issue.png)

## 5. Создание ветки из issue
1. Откройте созданный issue
2. Нажмите **"Create merge request"** в правом верхнем углу
3. Система предложит имя ветки вида `1-create-gitlab-manual`
4. Нажмите **"Create branch"**  
![Создание ветки из issue](screenshots/branch_from_issue.png)

## 6. Создание Merge Request в develop
1. После коммитов в ветке нажмите **"Create merge request"** (появится баннер)
2. Укажите:
   - Source branch: ваша ветка
   - Target branch: `develop`
3. Добавьте описание
4. Нажмите **"Create merge request"**  
![Создание MR](screenshots/create_mr.png)

## 7. Ревью и принятие MR
1. В Merge Request перейдите на вкладку **"Changes"**
2. Добавьте комментарии к коду (наведите на строку → **Comment**)
3. После правок нажмите **"Resolve thread"** для каждого комментария
4. Примите MR: **"Merge"** → **"Merge when pipeline succeeds"**  
![Принятие MR](screenshots/accept_mr.png)

## 8. Релиз версии в master
1. Создайте новый MR: `develop` → `master`
2. После мержа перейдите: **Repository → Tags**
3. Нажмите **"New tag"**
4. Укажите:
   - Tag name: `v1.0.0`
   - Message: `Стабильная версия мануала`
5. Нажмите **"Create tag"**  
![Создание тега](screenshots/create_tag.png)

## 9. Работа с Wiki
1. В меню проекта выберите **Wiki**
2. Нажмите **"Create your first page"**
3. Используйте Markdown-разметку:
   ```markdown
   # Заголовок
   - Список
   [Ссылка](https://example.com)