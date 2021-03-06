### Спецификации ОС

* Желательно использовать за основу дистрибютив на основе Debian/Ubuntu, предпочтение:
  * MX Linux (XFCE)
  * Lubuntu (LXQt)

* Не использовать SWAP партицию или файл!
* Все основные папки (/home,/root,/boot) и желательно и сам GRUB в одну партицию с размером не более 56Gb!
* выбрать на свое усмотрение тот формат партиции что лучше (надежнее и шустрее) срабатывает!
  
* Основная идея - экономить ресурсы - потому удалить все что касается:
  * gaming
  * office
  * paint
  * calendars
  * administrative tools

* Отключить автоматическое обновление

* Установить:
  * Python 3.8+ 64bit
  * Open JDK 11.x+ 64bit
  * C/C++ GCC/G++ последних версий 64bit
  * Node.js 13.x+ 64bit
  * PHP 7.4+ 64bit
  * MariaDB 10.4.x+ 64bit
  * Postgres 12.1+ 64bit
  * Git 2.2+ 64bit
  * nginx
   
* Установить:
  * Atom 1.43+ 64bit
  * Vscode 1.41+ 64bit
  * Brackets 1.41+ 64bit

* Установить:
  * veyon (classroom management)

* Установить:
  * Chrome 64bit свежую версию
  * Firefox 64bit свежую версию

* Отключить:
  * Любые ненужные эффекты манажера окон и граф интерфейса (тени, градиенты, размытье и т д)
  * Ненужные сервисы (apport,ufw,...)
  * авто запуск mysql,postgres,nginx!

---
### Самое Важное!
* Создать следующих пользователей в системе :
  * administrator/root -> sudoers group
  * trainer -> sudoers group, trainers group
  * ######################################
  * web-fe-dev -> students group    
  * web-be-dev -> students group    
  * java-dev -> students group    
  * python-dev -> students group    
  * c-dev -> students group    
  * cpp-dev -> students group    
  * ######################################
  * БЫЛО БЫ ХОРОШО ПОСЛЕ BOOT-a системы чтобы появилась окно логина откуда можно было бы выбирать "кем" залогинится (там только представители trainers и students!)
  * ВСЕ СТУДЕНТЫ БЕЗ ПАРОЛЕЙ!
  * ВСЕ ОСТАЛЬНЫЕ С ПАРОЛЯМИ!
  * СОЗДАТЬ В каждом ./home папку PROJECTS/ и ярлык для нее на рабочем столе
  * ИЗОЛИРОВАТЬ ПРАВА на "ЗАПИСЬ" НА ДОМАШНИЕ ПАПКИ ДЛЯ ВСЕХ ПОЛЬЗОВАТЕЛЕЙ!
  * УБЕДИТЬСЯ В ТОМ ЧТО USB/Flash автомонтируется и октрывается в проводнике!
  * С целью того чтобы экономить ресурсы создать shell-скрипты готовые к запуску определенных системных сервисов для каждого пользователя (пока можно макет их настроить, мы потом будем их тюнить)
  * Для всех основных приложений (atom,vscode,chrome,firefox) создать ярлык в быстрый запуск для каждого пользователя по отдельности чтобы можно было тюнить параметры запуска
  * Создать каждому пользователю свой .profile 
  * Создать  shell-скрипты которые очистят все что лишнее в Downloads/Desktop при каждом LOGIN/LOGOUT тех что в группе "students"
  

  
* Под самый конец было бы не плохо создать образ clonezill-Ой или каким-то похожим иснтрументом так чтобы можно было с флэшки ресетнуть систему за максимум 10-20 минут