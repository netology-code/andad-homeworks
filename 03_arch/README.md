# Домашнее задание к занятию «1.3 Architecture Components (часть 2)»

В качестве результата пришлите ссылки на ваш GitHub-проект в личном кабинете студента на сайте [netology.ru](https://netology.ru).

**Важно**: ознакомьтесь со ссылками, представленными на главной странице [репозитория с домашними заданиями](../README.md).

**Важно**: если у вас что-то не получилось, то оформляйте Issue [по установленным правилам](../report-requirements.md).

## Как сдавать задачи

1. Откройте ваш проект Android приложения с предыдущего ДЗ (можете брать код с лекции).
1. Сделайте необходимые коммиты.
1. Сделайте пуш (удостоверьтесь, что ваш код появился на GitHub).
1. Ссылку на ваш проект отправьте в личном кабинете на сайте [netology.ru](https://netology.ru).
1. Задачи, отмеченные, как необязательные, можно не сдавать, это не повлияет на получение зачета.

## Задача Refresh to Prepend

### Описание

Измените код с лекции так, чтобы:
1. Автоматический PREPEND был отключен (т.е. при scroll'е к первому сверху элементу данные автоматически не подгружались).
1. REFRESH не затирал предыдущий кеш, а добавлял данные сверху, учитывая id последнего поста сверху (соответственно, swipe to refresh должен "добавлять" данные, а не затирать их).
1. APPEND работал в обычном режиме.

Убедитесь, что ваше приложение нормально функционирует при следующих сценариях работы:
1. Чистая установка (БД пустая).
1. Запуск с заполненной БД (в БД остались данные с предыдущего запуска).

### Результат

Опубликуйте изменения в виде Pull Request'а в вашем проекте на GitHub.

В качестве результата пришлите: ссылку на PR GitHub-проект в личном кабинете студента на сайте [netology.ru](https://netology.ru)

## Задача Background Sync*

**Важно**: это необязательная задача. Ее (не)выполнение не влияет на получение зачета по ДЗ.

### Описание

В проекте с лекции отключена фоновая подгрузка постов с помощью `WorkManager`'а. Включите ее и обновите с учетом того, что в вашем приложении теперь есть `PostRemoteKeyDao` и фиксируются id'шники "последних" загруженных постов.

### Результат

Опубликуйте изменения в виде Pull Request'а в вашем проекте на GitHub.

В качестве результата пришлите: ссылку на PR GitHub-проект в личном кабинете студента на сайте [netology.ru](https://netology.ru)
