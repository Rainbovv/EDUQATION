## Классы. Динамическое использование - объекты. Отношения между классами (объектами)


> !!! Для решения этого примера - решить сначала [первую часть](./RESTAURANT.CL.DYN.ru.md)

---

* Дополним класс **Person** новым свойством (профессия - человека).
 
  ```java
  public class Person {
    // ...
    
    String jobTitle; // << + 

    // ...
  }
  ``` 
* Требуется:    
    - Установите для **jobTitle** сеттер и геттер.
    - Обновите код метода **printInfo()**, так чтобы он выводил
       
       ```John Doe (Designer): m, 31 years```   - если у него есть работа и

       ```John Doe: m, 31 years```   - если у него нет работы

 
* Обновляем структуру класса **Restaurant** (ресторан), дополним его одним всего лишь официантом (так как ресторан маленький). Свойство **waiter**:

 
  ```java
  public class Restaurant {
    // ...
    
    Person waiter; // << + 

    // ...  
  }
  ```  
  
* Требуется:
  1. Добавить сеттер / геттер для нового свойства:
  2. Обновить метод **printInfo()** который выводит в **out** имя ресторана, информацию об официанте, информацию о столах и данные о людях который сели за столами в таком формате
    
     ```
     RESTAURANT: Good Morning Sunshine!
     ##################################
     Thomas Kilk(Waiter): m, 30 years
     ----------------------------------
     Table: 1
     A) John Doe(Designer): m, 31 years
     B) Jane Doe: f, 30 years

     Table: 2
     A) John Doe(Tester): m, 31 years
     B) Free seat

     ...
     ``` 

--- 

* Ответьте на вопросы: 
  1. Сколько объектов максимально вмещает ресторан? а стол? человек? 
  2. Стоит ли назначать **jotTitle** в самом конструкторе **Person**?