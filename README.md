# Домашнее задание к занятию "Базы данных, их типы" - Еноктаев Олег


### Инструкция по выполнению домашнего задания

   1. Сделайте `fork` данного репозитория к себе в Github и переименуйте его по названию или номеру занятия, например, https://github.com/имя-вашего-репозитория/git-hw или  https://github.com/имя-вашего-репозитория/7-1-ansible-hw).
   2. Выполните клонирование данного репозитория к себе на ПК с помощью команды `git clone`.
   3. Выполните домашнее задание и заполните у себя локально этот файл README.md:
      - впишите вверху название занятия и вашу фамилию и имя
      - в каждом задании добавьте решение в требуемом виде (текст/код/скриншоты/ссылка)
      - для корректного добавления скриншотов воспользуйтесь [инструкцией "Как вставить скриншот в шаблон с решением](https://github.com/netology-code/sys-pattern-homework/blob/main/screen-instruction.md)
      - при оформлении используйте возможности языка разметки md (коротко об этом можно посмотреть в [инструкции  по MarkDown](https://github.com/netology-code/sys-pattern-homework/blob/main/md-instruction.md))
   4. После завершения работы над домашним заданием сделайте коммит (`git commit -m "comment"`) и отправьте его на Github (`git push origin`);
   5. Для проверки домашнего задания преподавателем в личном кабинете прикрепите и отправьте ссылку на решение в виде md-файла в вашем Github.
   6. Любые вопросы по выполнению заданий спрашивайте в чате учебной группы и/или в разделе “Вопросы по заданию” в личном кабинете.
   
Желаем успехов в выполнении домашнего задания!
   
# Задание 1. СУБД
Кейс
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

Приведите ответ в свободной форме.

# Задание 2. Транзакции
2.1. Пользователь пополняет баланс счёта телефона, распишите пошагово, какие действия должны произойти для того, чтобы транзакция завершилась успешно. Ориентируйтесь на шесть действий.

2.1.* Какие действия должны произойти, если пополнение счёта телефона происходило бы через автоплатёж?

Приведите ответ в свободной форме.

# Задание 3. SQL vs NoSQL
3.1. Напишите пять преимуществ SQL-систем по отношению к NoSQL.

3.1.* Какие, на ваш взгляд, преимущества у NewSQL систем перед SQL и NoSQL.

Приведите ответ в свободной форме.

# Задание 4. Кластеры
Необходимо производить большое количество вычислений при работе с огромным количеством данных, под эту задачу выделено 1000 машин.

На основе какого критерия будете выбирать тип СУБД и какая модель распределённых вычислений здесь справится лучше всего и почему?

Приведите ответ в свободной форме.

# Задание 1 ответ:
Для решения задач крупной строительной компании, занимающейся проектированием, девелопментом и управлением проектами, нужно подобрать правильные базы данных (СУБД). Вот какие типы СУБД подойдут для разных задач и почему:

### [1.1.] Финансовое планирование и отчетность.
Для точного учета финансов и подготовки отчетов нужна надежная база данных, которая гарантирует безопасность и порядок данных. Лучше всего подойдет **реляционная база данных** (RDBMS), например, **PostgreSQL** или **Microsoft SQL Server**. Эти базы помогают строить сложные финансовые модели и точно отслеживать риски.

*Если процесс шифрования данных занимает много времени, можно ускорить его с помощью библиотек для параллельных вычислений, таких как **OpenMP** или **TBB**.*

### [1.2.] Сбор данных с сайтов (лендинги) и работа с клиентами (CRM).
Для лендинга, куда поступают заявки клиентов, лучше использовать **NoSQL базу данных**, например, **MongoDB** или **Cassandra**. Они работают быстрее и удобнее с большими объемами данных. А для CRM-системы, где важен точный учет клиентских данных, лучше подойдет **MySQL** или **PostgreSQL**.

*Теоретически можно объединить обе задачи в одной базе данных, но это усложнит систему. Лучше разделить лендинги и CRM разными базами данных.*

### [1.3.] База знаний для внутренних стандартов и обучения.
Для хранения внутренней документации и учебных материалов достаточно простой базы данных, такой как **SQLite** или **PostgreSQL**. Они просты в управлении и поддерживают четкую структуру данных.

*Можно использовать уже существующие базы данных из других задач, если правильно организовать разделение данных и доступ.*

### [1.4.] Логистика и доставка.
Для планирования маршрутов и распределения ресурсов в логистике удобно применять **графовую базу данных**, например, **Neo4j**. Такие базы данных хорошо справляются с анализом связей между объектами, что важно для оптимизации маршрутов.

*Отдел закупок тоже может использовать базу данных логистов, если задачи взаимосвязаны. Но иногда лучше иметь отдельные базы данных для каждой группы задач.*

### [1.5.]  Общее решение.
Одну базу данных для всех задач использовать трудно, ведь каждая задача требует особого подхода. Лучше комбинировать разные типы баз данных: **реляционные** для финансов и CRM, **NoSQL** для лендинга, **графовые** для логистики. Так получится эффективнее и гибче управлять всеми данными.

# Задание 2 ответ
2.1. Пополнение баланса счёта телефона: успешная транзакция
При пополнении счета телефона обычным способом происходят следующие ключевые этапы:

1. Инициация платежа: Пользователь вводит номер телефона и сумму пополнения в платёжной системе (интернет-банк, мобильное приложение оператора и т.д.).
2. Проверка баланса: Платежная система проверяет, достаточно ли средств на счету пользователя для выполнения операции.
3. Запрос авторизации: Система запрашивает подтверждение транзакции (например, одноразовый код SMS, биометрическая проверка и т.д.).
4. Обработка платежа: После успешного подтверждения платеж отправляется оператору мобильной связи.
5. Уведомление оператора: Оператор получает уведомление о пополнении и зачисляет средства на счёт абонента.
6. Завершение транзакции: Пользователю приходит уведомление о завершении операции, а информация обновляется в личном кабинете.

2.2 Пополнение счёта телефона через автоплатёж
При настройке автоплатежа процесс выглядит следующим образом:

1. Настройка автоплатежа: Пользователь устанавливает параметры автоплатежа (сумма, периодичность и др.) в своём интернет-банке или приложении оператора.
2. Автоматический запуск платежа: По достижении определённых условий (например, когда баланс ниже установленного минимума) инициируется автоматическое пополнение.
3. Проверка баланса: Счёт пользователя проверяется на наличие достаточного количества средств для списания.
4. Авторизация не требуется: Поскольку автоплатёж заранее согласован, дополнительные подтверждения не нужны.
5. Платеж отправляется оператору: Средства списываются со счёта пользователя и отправляются оператору.
6. Зачисление и уведомление: Средства зачисляются на телефонный счёт, а пользователь получает уведомление о проведённой операции.
Таким образом, автоплатёж значительно упрощает процесс, делая его автоматическим и бесшовным для пользователя.

# Задание 3 ответ
3.1. Плюсы SQL-систем перед NoSQL
Четкая структура данных: SQL следит за порядком и структурой данных, что помогает избегать ошибок и повышает качество информации.
Надежные операции: SQL защищает данные при выполнении множества одновременных операций, гарантируя их точность и сохранность.
Один язык для всех: SQL — универсальный язык для работы с данными, который понимают почти все современные базы данных.
Быстрая обработка запросов: SQL хорошо справляется с сложными запросами благодаря специальным инструментам для ускорения поиска данных.
Надежность: SQL давно известен своей стабильностью и устойчивостью к сбоям.
3.1.* Плюсы NewSQL перед SQL и NoSQL
NewSQL объединяет достоинства SQL и NoSQL, предоставляя несколько важных преимуществ:

Легко расширять: NewSQL позволяет добавлять новые мощности и обрабатывать больше данных, как это делает NoSQL.
Надёжные операции: NewSQL, как и SQL, гарантирует сохранение данных даже при большом количестве операций одновременно.
Простота перехода: NewSQL работает с языком SQL, что делает его удобным для тех, кто уже знаком с классическими базами данных.
Высокая скорость: NewSQL обрабатывает данные быстрее, чем традиционные SQL-системы, благодаря новым технологиям.
Гибкость: NewSQL может работать как с жестко структурированными, так и с менее упорядоченными данными, что делает его универсальным решением.
Таким образом, NewSQL сочетает лучшее от обоих миров: простоту SQL и гибкость NoSQL.

# Задание 4 ответ:

Чтобы выбрать подходящую базу данных (СУБД) и модель вычислений для работы с большим объемом данных на 1000 машинах, нужно учитывать несколько факторов: скорость обработки, возможность расширения и устойчивость к сбоям.

### Лучший выбор СУБД

Для таких задач отлично подходят **распределённые СУБД**, которые умеют делить данные и вычисления между машинами. Примеры таких систем:

- **Hadoop**: Хорошо подходит для долгой обработки больших наборов данных. Использует технологию MapReduce, которая делит задачи на маленькие части и выполняет их параллельно.
  
- **Apache Spark**: Более современный вариант, который быстрее Hadoop и умеет работать с потоками данных в реальном времени.

- **Cassandra**: Это база данных, которая хорошо справляется с записью и чтением данных в больших объемах. Она особенно хороша для случаев, когда нужно постоянно добавлять новые данные.

### Почему они подходят

Эти системы хорошо справляются с задачей благодаря нескольким причинам:

1. **Скорость**: Они могут распределять задачи между тысячами компьютеров, что ускоряет обработку данных.

2. **Надежность**: Даже если одна машина выйдет из строя, остальные продолжат работу, и данные не потеряются.

3. **Удобство расширения**: Если понадобится добавить больше машин, это можно сделать без остановки работы всей системы.

Таким образом, для вашей задачи лучше всего подойдут **Hadoop или Spark**, потому что они созданы для быстрой и надежной работы с огромными объемами данных на множестве машин.
