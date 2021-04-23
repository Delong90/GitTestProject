# GIT INFO
## Создание TOKIN для входа в аккаунт через AndroidStudio
Может понадобиться при ошибке входа через пароль, так же можно отредактировать доступ к определённым возможностям
[Создание TOKIN](https://docs.github.com/en/github/authenticating-to-github/creating-a-personal-access-token)
## Этап создания репозитория и отправки изменений в удалённый репозиторий
1. Для получения информации о возможностях комманды необходимо в консоле прописать

    **git <комманда> -h** *: к примеру git add -h выдаст в консоле возможности комманды добавления файлов*

2. При старте нам необходимо создать локальный репозиторий на компе, это выполнятется коммандой

    **git init**    *: происходит инициализация в той папке в которой создан проект*

3. После создания репозитория нам небходимо добавить файлы которые будут иметь связь с репозизиторием

    **git add .**   *: добавляет все файлы кроме прописанных в игноре*

4. Далее необходимо описать сообщением те изменения которые были внесены

    **git commit -m "текст сообщения"**   *: флаг -m обозначает сообщение message*

5. При создании репозитория у нас отсутствуют ветки(либо имеет дефолтное имя), следовательно создаём ветку в которой будем работать

    **git branch -M main**   *: создание ветки с именем main, -M обозначает переименовать ветку*

6. Задание удалённого репозитория

    **git remote add origin https://github.com/Delong90/GitTestProject.git** *: добавить удалённый репозиторий с именем необходимым для обращения к нему origin(дефолтное имя если мы выполняли clone, с адресом https://github.com/Delong90/GitTestProject.git)*

8. Отправка изменений в удалённый репозиторий

    **git push -u origin main** *: отправить существующие коммиты по ветку main на удалённый репозиторий origin -u вродебы означает --set-upstream запуск потока*

## Проверка наличия отличий удалённого репозитория и локального, вытягивание изменений

1. Проверка изменений

    **git fetch** *: получить данные о изменениях*

    **git diff main origin/main** *: вывод информации о различиях между веткой локальной веткой main и веткой origin/main на удалённом репозитории*

    **git pull** *: вытягивание из удалённого репозитория, обновление файлов сработает при условии что в файлы которые должны вытянуться ты не вносил изменения*

## Работа с ветками

**git branch** *: инфо о ветках*

**git branch name** *: создание ветки name*

**git checkout name** *: переход на ветку name*

**git checkout –b name** *: создание ветки name и переход на неё*

**git merge main** *: замерджить изменения из main в ветку на которой ты находишься и создаст новы commit*

**git merge main feature** *: замержить из main и перейти на feature и создаст новы commit *

**git checkout feature** *: переход на ветку feature*
**git rebase main** *: начинает ветку с последнего изменения main(переносит ветку вперёд) влить  изменения main в ветку feature, коммиты обновляются*

**git checkout feature** *: переход на ветку feature*
**git rebase –i main** *: то же что и выше но дополнительно объединяет лишние комминты(из 3 получаем 2 коммита)*

**git push --force** *: делается после rebase*

**git checkout feature** *: переход на ветку feature*
**git rebase –i HEAD~3** *: rebase три коммита в один*
# GIT ADVANCED


**** *: *

