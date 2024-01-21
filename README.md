# Lab_2
Концептуальная модель:
На основе анализа предметной области "Управление складскими запасами", были выделены следующие информационные объекты, которые необходимо хранить в базе данных:
1. Категория товара (Category)
2. Товар (Product)
3. Отчёт о спросе (Demand report)
4. Пользователь (User)
5. Роль (Role)
6. Задача (Task)

Логическая модель:
На основе концептуальной модели, была построена логическая модель базы данных для онлайн-сервиса "Управление складскими запасами", состоящая из следующих информационных объектов:

1.Category
category_id (bigint, PK) - идентификатор категории
category_name (varchar(255)) - название категории
category_description (varchar(255)) - описание категории
2. Product
product_id (bigint, PK) - идентификатор товара
product_name (varchar(255)) - название товара
arrival_date (varchar(30)) - дата поступления
consumption_date (varchar(30)) - дата расходования
amount (int) - количество
category_id (bigint, FK) - внешний ключ для связи с таблицей "Category"
3. Demand report
report_id (bigint, PK) - идентификатор отчёта
date (varchar(30)) - дата создания
min_value (int) - количество min
max_value (int) - количество max
product_id (bigint, FK) - внешний ключ для связи с таблицей "Product"
4. User
user_id (bigint, PK) - идентификатор пользователя
username (varchar(30)) - имя пользователя
user_role_id (bigint, FK) - внешний ключ для связи с таблицей "Role"
5. Role
user_role_id (bigint, PK) - идентификатор роли
user_role_name (varchar(30)) - название роли
6. Task
task_id (bigint, PK) - идентификатор задачи
task_name (varchar(30)) - название задачи
user_role_id (bigint, FK) - внешний ключ для связи с таблицей "Role"
category_id (bigint, FK) - внешний ключ для связи с таблицей "Category"
product_id (bigint, FK) - внешний ключ для связи с таблицей "Product"
report_id (bigint, FK) - внешний ключ для связи с таблицей "Demand report"
status (boolean) - статус задачи
