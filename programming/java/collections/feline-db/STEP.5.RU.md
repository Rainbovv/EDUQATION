## База данных с кошками

* Доделаем метод **save(...)** репозитория. Этот метод должен работать по очень простой схеме:

   1. Найти объект в списке репозитория при помощи переданного ```feline.getId()```
   2. Если объект не найден, добавить его в конец списка (в конец внутренней коллекции), вернуть **true** чтобы просигналить о том что все удачно прошло
   3. Если объект найден, то обратиться у существующему **update(...)**, в данном случае **save(...)** просто "закрепит" изменения в оригинал. Вернуть при этом **true**.

* Подумайте, можно ли переделать алгоритм **save(...)** так чтобы поиск элемента по списку не происходил 2 раза? (ведь пункт 1 его ищет, а так же функция **update(...)** тоже его ищет)