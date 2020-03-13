# Задание: 

## 0. Компоненты:
* Laravel 6.*
* MySQL

## 1. Вводное:

1. Создать модель `User` без кастомных полей  
2. Создать модель `Article` с полем `text`  
3. Добавить отношение "многие ко многим":  
4. Написать свойство `articles` в первой модели, которое вернёт все статьи пользователя  
5. Написать метод `users` во второй, которое вернёт всех авторов статьи 

## 2. Работа с формами и запросами

1. Расширить модель `User`, чтобы она имела поля, соответствющие форме index.html
2. Доработать приложение, чтобы данные с этой формы создавали объект `User` в базе данных на сервере
3. После сохранения данных на сервере происходит редирект на точно такую-же страницу, где данные уже введены и их нельзя изменить

## 3. Мягкое удаление:

1. Добавить возможность удалять статьи в мягком режиме 

## 4. Методы и строгая типизация:

Теперь надо создать метод в классе статей, которая:

1. Принимает пользователя и только пользователя - выдаёт mismatch exception в противном случае
2. Возвращает  
    - истину если указанный человек автор статьи  
    - ложь - если это не так  
    - null если статья удалена  
3. Если функция пытается вернуть что - то иное - mismatch exception

## 5. ORM. Теоритический вопрос:
Добавим новое поле пользователю experience. Есть функция, в которой: 
1. Будет извлекаться пользователь и сохраняться в переменную `$user = User::find(1)`  
2. Дальше функция выводит `experience`
3. Параллельно с работой функции асинхронный метод меняет опыт на случайное число каждые несколько секунд  

В первой функции ещё раз выводится спустя промежуток времени опыт пользователя.  Каким будет этот вывод ?  
    
## 6. Загрузить на гитхаб в публичный репозиторий и отправить ссылку.

Желаем Вам удачи!
