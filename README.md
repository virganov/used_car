## Project's objectives
Many areas in Indonesia doesnt have efficient and reliable public transportation, its leading people to prefer using private transportation such as four-wheeled vehicles or two-wheeled vehicles. However, this project specifically concentrates on four-wheeled vehicles or cars. In line with the inadequate public transportation in Indonesia, the demand for cars is increasing, and buying and selling used cars has become quite popular for people who need a four-wheeled vehicle but have a limited budget. In this digital era, the online buying and selling of used cars provide sellers to advertise widely through a platform and connects with potential buyers. This project focuses on establishing database for the sale of used cars. 
The aim of this article is to design a database system for selling the used cars with well-organized structure.

## Designing The Database
In designing the database, the first step is to determine the mission statement. The mission statement for this project is as follows:
1. Users can advertise used cars.
2. Users can place bids on the advertised cars.

This project has some limitations, including:
1. Each user of the application can advertise more than one product.
2. Every user can search for offered cars based on the seller's location, car brand, and body type.
3. If a potential buyer is interested in a car, they can bid on the product if the seller allows the bidding feature.
4. Purchase transactions are conducted outside the application and are not within the project scope.

After that, we create tables related to the e-library system and determine their relationships through the definition of primary keys and foreign keys. The following is the ERD that I made, with a description of each table.

cities table : this table stores information about locations. It has a primary key (PK) in column city_id, that uniquely indentifying each city. it also has city columns for the name of city, columnlatitude and longitude for geographic coordinate.
products table : this table stores information about the the product or cars. It has a primary key (PK) in column product_id, that uniquely indentifying each products. Others columns are merk , model , body_type , car_type , years and price to store informations about product's data.
users table : this table stores information about the the user of this platform. It has a primary key (PK) in column user_id, that uniquely indentifying each users. It also has city_id as foreign key (FK) referencing from city_idin citiestable.  Others columns are first_name , last_name and phone to store informations about user's data.
advertisements table : this table stores information about the advertisement that has been posted by the user. It has a primary key (PK) in column ads_id, that uniquely indentifying each ads. It also has product_id as foreign key (FK) referencing from product_id in productstable, user_id as foreign key (FK) referencing from user_id in userstable, title columns contains the title of the ads, date_post for time the ads posted.
bids table : this table stores information about the bids from user as potensial buyers of the products. It has a primary key (PK) in column bid_id, that uniquely indentifying each bids from users. It also has user_id as foreign key (FK) referencing from user_id in userstable, product_id as foreign key (FK) referencing from product_id in productstable, date_bid columns for the time the bid is given, bid_price for price for bid that has been submited by the user , bid_status for the status of bid, it contains sent or failed.
