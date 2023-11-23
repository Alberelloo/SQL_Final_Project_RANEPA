# SQL_Final_Project_RANEPA
Final project on <b>SQL</b>:

Task 1. Create PostgreSQL server with with Docker

Task 2. Come up with Database (6+ tables, minimum 1 many-to-many relationship) that applicable to any real business

Task 3. Generate/Parse data and dump to DB

Task 4. Write 3 complex queries, counting different slices/metrics

Task 5. Visualize data from the queries


______________
<b>Stack</b>: Python, Docker, Requests, lxml, Psycorg2, SQLAlchemy
______________
* A business chosen for the project: maxtix-produced custom details for cars
* Database contains 7 tables:

| Название таблицы  | Колонки | Связанные таблицы |
| ------------- | ------------- | ------------- |
| customer | client_id,full_name,gender,phone_number,job,birth,email,company | order_details | 
| order_details | client_id,order_id,deliv_city,order_date,positions,value,status|customer,payment_details,city,orders |
| orders | order_id,car_model,car_year,car_category,color,att_photos,car_prod| order_details, order_detail |
| payment_details |order_id,bank,credit_card_provider,checking_account| order_details |
| order_detail | order_id,detail | orders,details |
| details| detail,category | order_detail |
| city |city_name,latitude,longtitude |order_details |

* List of detail was parsed from the Internet, the other data was generated with Faker
* Visualization was provided with <b>Power BI</b> (photo were not taken -> not atteched)
