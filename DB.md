# Домашнее задание к занятию «Базы данных, их типы»-Тихомиров Алексей


# Задание 1. СУБД
### Кейс
Крупная строительная компания, которая также занимается проектированием и девелопментом, решила создать правильную архитектуру для работы с данными. Ниже представлены задачи, которые необходимо решить для каждой предметной области.
Какие типы СУБД, на ваш взгляд, лучше всего подойдут для решения этих задач и почему?

1.1. Бюджетирование проектов с дальнейшим формированием финансовых аналитических отчётов и прогнозирования рисков. СУБД должна гарантировать целостность и чёткую структуру данных.

1.1.* Хеширование стало занимать длительно время, какое API можно использовать для ускорения работы?

1.2. Под каждый девелоперский проект создаётся отдельный лендинг, и все данные по лидам стекаются в CRM к маркетологам и менеджерам по продажам. Какой тип СУБД лучше использовать для лендингов и для CRM? СУБД должны быть гибкими и быстрыми.

1.2.* Можно ли эту задачу закрыть одной СУБД? И если да, то какой именно СУБД и какой реализацией?

1.3. Отдел контроля качества решил создать базу по корпоративным нормам и правилам, обучающему материалу и так далее, сформированную согласно структуре компании. СУБД должна иметь простую и понятную структуру.

1.3.* Можно ли под эту задачу использовать уже существующую СУБД из задач выше и если да, то как лучше это реализовать?

1.4. Департамент логистики нуждается в решении задач по быстрому формированию маршрутов доставки материалов по объектам и распределению курьеров по маршрутам с доставкой документов. СУБД должна уметь быстро работать со связями.

1.4.* Можно ли к этой СУБД подключить отдел закупок или для них лучше сформировать свою СУБД в связке с СУБД логистов?

1.5.* Можно ли все перечисленные выше задачи решить, используя одну СУБД? Если да, то какую именно?

### Ответ : 
```
1.1. Реляционная СУБД - Oracle или Microsoft SQL. Можем использовать аналитические функции, доступные в этих СУБД, для прогнозирования рисков.  
1.2. NoSQL, например MongoDB или Cassandra. Имеется гибкость и быстродействие, подходит для большого объема данных.
1.3. PostgreSQL или MySQL так как требуется простая и понятная структура данных.
1.4. OrientDB для быстрой работы со связями.  
```

### Задание 2. Транзакции
2.1. Пользователь пополняет баланс счёта телефона, распишите пошагово, какие действия должны произойти для того, чтобы транзакция завершилась успешно. Ориентируйтесь на шесть действий.

2.1.* Какие действия должны произойти, если пополнение счёта телефона происходило бы через автоплатёж?
Приведите ответ в свободной форме.

### Ответ : 
```
2.1.   
1. Пользователь выбирает способ пополнения баланса счета телефона 
2. Пользователь указывает сумму, которую он хочет пополнить.
3. Пользователь вводит данные своего банковского счета 
4. Система проверяет правильность введенных данных и наличие достаточного количества средств для совершения транзакции.
5. После успешной проверки система списывает сумму с банковского счета пользователя и зачисляет ее на баланс телефона
6. Пользователь получает уведомление об успешном пополнении баланса счета телефона
```

### Задание 3. SQL vs NoSQL
3.1. Напишите пять преимуществ SQL-систем по отношению к NoSQL.

3.1.* Какие, на ваш взгляд, преимущества у NewSQL систем перед SQL и NoSQL.
Приведите ответ в свободной форме.

### Ответ : 
```
3.1.  
1. Ограничения целостности данных, что дает сохранность и защиту от ошибок ввода.  
2. Быстрое создание и изменение БД.  
3. При небольших объемах производительность весьма высока.  
4. Много инструментов и библиотек в силу большой распространенности.  
5. Транзакции гарантируют целостность и защиту от сбоев.  

```

### Задание 4. Кластеры
Необходимо производить большое количество вычислений при работе с огромным количеством данных, под эту задачу выделено 1000 машин.
На основе какого критерия будете выбирать тип СУБД и какая модель распределённых вычислений здесь справится лучше всего и почему?
Приведите ответ в свободной форме.

### Ответ : 
```
Ряд критериев :
1. Высокая скорость обработки данных
2. Высокая производительность
3. Надежность
4. Удобство
Для выделенных критериев подходит Apache Cassandra. 
```
