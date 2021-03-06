## Имплементирование на уровне JPA используя Hibernate ORM

> Использование полиморфных отношений при помощи @Any, @ManyToAny. Дело в том что другие типы связей дают возможность связать через одну и ту же связь только сущности класса на уровне которого была объявлена связь, а так же наследников класса! А что если требуется привязать один тип сущности к двум разным классам (не родственникам)? Тогда используются полиморфные отношения.

### Cедьмая ЧАСТЬ

материалы:
 - [1](https://docs.jboss.org/hibernate/orm/5.4/userguide/html_single/Hibernate_User_Guide.html#associations-any)


* Предположим есть класс **Award** (награда), сущность с свойствами:
  1. String title (титул)  
  2. Date date (дата - когда ее отдали)
  3. Enum type (тип награды - например: MEDAL, TROPHY, DIMPLOMA, ... )
* Объявите данную сущность
* Предположим наградить могут как студента (Student) и всех его наследников, так и группу (Group), так и факультет (Faculty) 
* Требуется добавить ОДНОСТОРОННЮЮ полиморфную связь (@Any) со стороны **Award**, связанную с любым из перечисленных выше объектом!
* Проверку сдалеть так:
  1. Наградить какого-нибудь студента медалью за успешные результаты!
  2. Наградить группу студентов Трофеем за топовый результаты!
  3. Наградить факультет Дипломом за самый высокий процентаж трудоустройства! 
---



