//Task-1

1.select title from movies;
2.select director from movies;
3.select title,director from movies;
4.select title,year from movies;
5.select \* from movies;
![alt text](<Screenshot (11).png>)

//task-2

![alt text](<Screenshot (13).png>)
1.SELECT Title from movies where id=6;
2.SELECT Title from movies where year between 2000 and 2010;
3.SELECT Title from movies where year not between 2000 and 2010;
4.SELECT Title,Year FROM movies where id between 1 and 5;

//Task-3

1.SELECT Title FROM movies where Title Like "Toy%";
2.SELECT Title FROM movies where Director Like "John Lasseter";
3.SELECT Title,Director FROM movies where Director not Like "John Lasseter";
4.SELECT Title FROM movies where Title like "%WALL%";
![alt text](<Screenshot (14).png>)

//Task-4

1.SELECT Distinct Director FROM movies;
2.SELECT Title FROM movies order by Year Desc Limit 4 ;
3.SELECT Title FROM movies order by Title Asc limit 5;
4.SELECT \* FROM movies order by Title Asc Limit 5 offset 5;
![alt text](<Screenshot (15).png>)

//Task-5

1.SELECT city,Population FROM north_american_cities where country Like "canada";
2.SELECT City FROM north_american_cities where country Like "United States" order by latitude Desc;
3.SELECT City,Longitude FROM north_american_cities where longitude<(select longitude from North_american_cities where City like "chi%")order by Longitude Asc;
4.SELECT Top 2 City FROM north_american_cities where country Like "mex%" order by population Desc;
5.SELECT City,Population FROM north_american_cities order by Population Desc, country Like "Uni%" Limit 2 offset 4;
![alt text](<Screenshot (16).png>)

//Task-6

1.SELECT Title ,Domestic_sales, International_sales FROM Movies Inner Join Boxoffice on Movies.Id=Boxoffice.Movie_Id;
2.SELECT Title, Domestic_sales,International_sales FROM Movies Inner Join Boxoffice on Movies.Id=Boxoffice.Movie_Id where International_sales>Domestic_sales;
3.SELECT Title,Rating FROM Movies Inner Join Boxoffice on Movies.Id=Boxoffice.Movie_Id Order by Rating Desc;
![alt text](<Screenshot (17).png>)

//Task-7
1.select distinct Building from Employees;
2.select Building_name,Capacity from Buildings
3.select distinct Building_name,Role from Buildings left join employees on building_name=building;
![alt text](<Screenshot (20).png>)

//Task-8

1.SELECT Name,Role FROM employees where Building is Null;
2.SELECT Building_name from Buildings left join Employees on building_name=building where building is null
![alt text](<Screenshot (21).png>)

//Task-9

1.SELECT Title,((Domestic_sales+International_sales)/1000000) as combined_sales from Movies Inner join boxoffice on Id=Movie_id;
2.SELECT Title,Rating\*10 as percent from Movies Inner join boxoffice on Id=Movie_id;
3.SELECT title, year
FROM movies
WHERE year % 2 = 0;
![alt text](<Screenshot (22).png>)

//Task-10
1.SELECT Years_employed from Employees order by Years_employed Desc limit 1;
2.select distinct role,AVG(Years_employed) as years from employees group by role;
3.select Building,sum (years_employed) from employees group by building
![alt text](<Screenshot (23).png>)

//Task-11
