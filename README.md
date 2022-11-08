# DB_2022
## 1.	Тема разрабатываемого в семестре проекта:
Интернет магазин

## 2.	Функциональные требования к проекту:
В программе существует 2 вида пользователей: администратор (admin), покупатель (user).  
Доступные всем команды:  
•	Регистрация  
•	Вход  
•	Просмотр списка товаров  

## 1.	Администратор:  
•	Просмотр списка всех сделок  
•	Изменение статуса «Есть в наличии»  
•	Добавление новых моделей  
•	Добавление новых категорий  
•	Добавление количества товаров  

## 2.	Покупатель  
•	Возможность приобрести товар  
•	Просмотр суммы, потраченной на покупку  
•	Просмотр истории своих заказов  
•	Выставление оценки товару  
  
## 3. В БД присутствуют следующие сущности:  
•	Product – товар, который располагается на сайте.
    product_id int (PK),   
    category_id int NOT NULL (FK1),  
    discount_id int NOT NULL (FK2),  
    size_id int NOT NULL (FK3),  
    title varchar(100) NOT NULL,  
    description varchar(100) NOT NULL,   
    image varchar(100) NOT NULL,     
    price int NOT NULL,   
       
•	Category – категория товаров.  
    category_id int (PK),  
    title varchar(30) NOT NULL    
      
•	Size – размеры и их количество.  
    size_id int (PK),  
    size varchar(6) NOT NULL,  
    quantity int NOT NULL  
    
•	Discount – размер скидки.  
    discount_id int (PK),  
    discount int NOT NULL  
      
•	User – пользователь приложения.   
    user_id int (PK)  
    permission_id int NOT NULL (PK),  
    firstname varchar(100) NOT NULL,  
    lastname varchar(100),  
    password varchar(100) NOT NULL,  
    phone varchar(100),  
    email varchar(50) NOT NULL   
      
•	Permission – уровень доступа пользователя на сайте. Может быть обычный пользователь(user) и админ(admin).  
    permission_id int (PK)  
    title varchar(30) NOT NULL  
•	Orders  
    order_id int (PK),  
    user_id int NOT NULL (FK1),  
    product_id int NOT NULL (FK2)  
      
•	Cart – корзина с покупками пользователя.  
    card_id int (PK),  
    user_id not NOT NULL (FK1),  
    product_id NOT NULL (FK2)  

