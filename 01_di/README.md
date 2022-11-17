# Домашнее задание к занятию «1.1. Dependency Injection»

В качестве результата пришлите ссылки на ваш GitHub-проект в личном кабинете студента на сайте [netology.ru](https://netology.ru).

**Важно**: ознакомьтесь со ссылками на главной странице [репозитория с домашними заданиями](../README.md).

**Важно**: если у вас что-то не получилось, оформите Issue [по установленным правилам](../report-requirements.md).

## Как сдавать задачи

1. Откройте ваш проект Android-приложения из предыдущего ДЗ (можете брать код с лекции).
1. Сделайте необходимые коммиты.
1. Сделайте push. Убедитесь, что ваш код появился на GitHub.
1. Ссылку на ваш проект отправьте в личном кабинете на сайте [netology.ru](https://netology.ru).
1. Задачи, отмеченные как необязательные, можно не сдавать. Это не повлияет на получение зачёта. В этом ДЗ все задачи обязательные.

## Задача №1. Dagger Hilt

### Описание

Проведите миграцию вашего проекта на Dagger Hilt. Функционал и автотесты должны работать без изменений.

## Задача №2. Singletons

### Описание

В приложении с лекции в `MainActivity` используются следующие конструкции:

```kotlin
FirebaseMessaging.getInstance().token.addOnCompleteListener { task ->
    ...
}

with(GoogleApiAvailability.getInstance()) {
    ...
}
```

Замените вызовы `getInstance` на DI. Для этого напишите собственные модули.

### Результат

Опубликуйте изменения в виде Pull Request в вашем проекте на GitHub.

В качестве результата пришлите ссылку на PR GitHub-проект в личном кабинете студента на сайте [netology.ru](https://netology.ru).


### Возможные проблемы и их решения

1. Если во время выполнения происходит следующее исключение
<img width="1097" alt="image" src="https://user-images.githubusercontent.com/13727567/202386286-f44b2849-55eb-4ae9-b790-8284e4f01d5a.png">
Проверьте, что вместо шаринга viewModel таким способом

```
private val viewModel: PostViewModel by viewModels(ownerProducer = :: requireParentFragment)
```
Вы используете функцию activityViewModels
```
private val viewModel: PostViewModel by activityViewModels()
```


2. При возникновении данной проблемы во сборки
<img width="1516" alt="image" src="https://user-images.githubusercontent.com/13727567/202386789-46a93331-9adf-48f1-82f5-93734337956c.png">
Проверьте, что вы используете актуальную версию hilt. Посмотреть можно [здесь](https://github.com/netology-code/andad-code/blob/master/01_di/android/build.gradle#L4)


3. Если при сборке вы видите следующее сообщение об ошибке,

![image](https://user-images.githubusercontent.com/13727567/124985798-8264b200-e043-11eb-96f6-cec2de608962.png)
но вы сделали всё по инструкции, проверьте версию Котлина. 
Если у вас 1.5.20, нужно обновиться до 1.5.21.
