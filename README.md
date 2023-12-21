## Домашнее задание к уроку Spring.

Нужно написать сервис, который собирает корзину для интернет-магазина.

Алгоритм действий:

 Разработайте контроллер, сервис и некую сущность корзины с покупками.
 У контроллера должны быть два метода:
/store/order/add

/store/order/get

 При обращении к методу add можно в качестве параметров запроса передавать один или несколько чисел, которые являются ID некоего товара.
 При get мы должны получить все добавленные ID в виде списка в JSON-формате.
 Для каждого подключения нового клиента должен создаваться новый объект — корзина.
 Никаких хранилищ всех корзин быть не должно.
 В качестве теста можно зайти со своего браузера и добавить итемы (item), далее — получить список.
 Этот же тест нужно проделать через браузер в режиме инкогнито и получить другой список.
Алгоритм действий теста в браузере в режиме инкогнито:

 Обращаемся к методу add из браузера, добавляем первые ID.
 Обращаемся к методу add из инкогнито, добавляем первые ID.
 Повторяем шаг 1 и 2.
 Обращаемся к методу get сначала из браузера, потом из инкогнито. Списки должны быть разными и заполнены тем, что было в шагах 1–3 .
Подсказки
 Нужно выбрать корректный скоуп для корзины.
 Нужно указать context-path /store в application.properties.
 Метод add должен быть один и при этом корректно работать как с одним ID, так и с несколькими.
 Учесть, что ID могут повторяться. Выбрать соответствующую коллекцию в корзине.
Критерии оценки
 Контроллер включает в себя два метода: /store/order/add и /store/order/get
 В метод add можно передавать только целочисленные значения
 При методе get выводится список ID всех записанных значений
 Для каждого нового клиента создается новый объект-корзина
 При проверке сервиса с браузера в режиме инкогнито пользователь получает другой список
