# Mobile-Sales-Analysis-Power-BI-and-SQL-project
This is a Power BI and SQL project to analyze the mobile sales and visually analyze the data using interactive dashboards.
KPIs

1. Check  mobile features and price list

   
select Phone_name, Price from mobile;


2. Price of 5 most expensive phones


select*from mobile
order by price desc
limit 5;


3. The price of 5 most cheapest phone


select* from mobile
order by price asc
limit 5;


4. Top 5 Samsung phones with price and all features


select* from mobile where brands="samsung"
order by price desc
limit 5;

5. Must have android phone list then top5 high price android phones


select*from mobile where Operating_System_Type="Android"
order by price desc
limit 5;


6. Android phone list then top 5 lower price


select*from mobile where Operating_System_Type="Android"
order by price asc
limit 5;

7.IOS phone list then top 5 high price IOS Phones


select*from mobile where Operating_System_Type="IOS"
order by price desc
limit 5;

8.IOS phone list then top 5 LOW price IOS Phones


select*from mobile where Operating_System_Type="IOS"
order by price asc
limit 5;

9. Phone support 5g and also top 5 phone with 5g support


select*from mobile where 5G_Availability="Yes"
order by price desc
limit 5;

10. Total price of all mobile is to be found with brand name

    
select brands, sum(price) from mobile group by brands;

