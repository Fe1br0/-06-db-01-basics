# Домашнее задание к занятию "6.1. Типы и структура СУБД"



## Задача 1



```
Электронные чеки в json виде здесь я бы выбрал NoSQL СУБД , например MongoDB т.к. отлично подходит для электронной коммерции

Склады и автомобильные дороги для логистической компании  тут мой выбор пал на Реляционные например Postgre из за высокой производительности и надежности

Генеалогические деревья - выберу Иерархические т.к. их структура изначально похоже на генеалогическое древо :)

Кэш идентификаторов клиентов с ограниченным временем жизни для движка аутенфикации - думаю в этом случае может подойти Ключ-значение

Отношения клиент-покупка для интернет-магазина - в этом примере думаю будет уместно использовать Графовые , т.к. она отлично подходит под задачи сбора и анализа 
разнородной информации такой как: предпочтений пользователей.,программы лояльности, SEO и т. д.

```



## Задача 2


```
- Данные записываются на все узлы с задержкой до часа (асинхронная запись) - По CAP-теореме: CA (согласованность данных и доступность) / По PACELC: PA/EC


- При сетевых сбоях, система может разделиться на 2 раздельных кластера  - По CAP-теореме: AP (согласованность данных и устойчивость к разделению) / По PACELC: PA-EL


- Система может не прислать корректный ответ или сбросить соединение - По CAP-теореме: CP (доступность и устойчивость к разделению) / По PACELC: PC-EC

```

## Задача 3


```
Думаю нет , т.к. эти 2 системы противоположны друг другу ACID более надежная но медленная , 
когда как BASE более быстрая но не всегда может давать корректные данные следовательно менее 
надежная в плане точности отдаваемых данных .
```

## Задача 4


```
Исходя из лекции это могли бы быть Memcached или Redis , но если речь идет о key-value хранилище ,
которое имеет механизм pub\sub то это  Redis , система pub\sub
это асинхронный метод связи между сервисами, используемый в бессерверных архитектурах и архитектурах 
микросервисов включает в себя : издателя который отправляет сообщения и подписчика который получает сообщения.
Из минусов могу отметить необходимость в большом количестве ОЗУ,отсутствие очередей сообщений.

```
## Доработка

```
Прочитав по Вашей рекомандации хабр , из минусов выделить могу: Redis хранит все данные в оперативной памяти, и при аварийном завершении процесса или выключении машины данные будут потеряны, даже при включённом сохранении на диск данные могут быть потеряны частично либо полностью, фоновое сохранение данных на диск может нанести ущерб производительности и отказоустойчивости.
```

