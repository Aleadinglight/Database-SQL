```
sqlite> .tables
```
1.Select all the countries
```
sqlite> .schema country
select * from country;
```
2.Select just all the country names
```
sqlite> select "name" from country;
```
3.Select name and capital of all the countries
```
sqlite> select "name","capital" from country;
```
4.Select just all the country names in descending mode (last alphabets first)
```
sqlite> select "name" from country order by name desc;
```
5.Select just all the country names just for five first countries
```
sqlite> select name from country limit 5;
```
6.Select just all the country names just for 100 first countries
```
sqlite> select name from country limit 100;
```
7.Select just all the country names but order the result by the country name
```
sqlite> select "name" from country order by name asc;
```
8.Select name of the countries where the name has 'ia'
```
sqlite> select name from country where name like "%ia";
```
9.Select region and the country names but order the result initially by the region and then by the country name
```
sqlite> select region,name from country order by region,name;
```
10.Select the country names ordered by the population, the biggest countries first
```
sqlite> select name from country order by surfacearea desc,population;
```
11.Select the name and the region of all the countries
```
sqlite> select name,region from country;
```
12.Find countries with the name starting with Y-letter
```
sqlite> select name from country where name like "Y%";
```
13.Find continent and name of countries where the continent is Europe
```
sqlite> select continent,name from country where continent="Europe";
```
14.Find continent and name of countries  where the continent is Europe or Asia
```
sqlite> select continent,name from country where continent="Europe" or continent="Asia";
```
15.Find region, name and population of the first biggest European counties by size
```
sqlite> select region,name,population from country order by surfacearea desc;
```	
16.Select the name and life expectancy of countries where life expectancy is more than 80
```
sqlite> select name,lifeexpectancy from country where lifeexpectancy>80;
```
17.Select the name and population of countries where the number of population is between 5 and 10 million people
```
sqlite> select name,lifeexpectancy from country where lifeexpectancy>80;
```
18.Select the name and population of countries where the number of population is between 5 and 10 million people that are in Europe ordered by population descending
```

```
select the names of countries that start with A-letter but do locate outside Europe
select the name and population of the country that has most of population
select the name and life expectancy of the country that has shortest life expectancy (not NULL one)
count the total number of population in the table
find all the Republic countries
find countries who became independent after 1975
find the ten oldest countries based on indepyear the name and year
select the current date and time (2017-01-11 09:01:20)
find out what is the current year (2017)
calculate how old is the oldest existing country (UK)
calculate how old will Finland be this year
find out how many countries there is where the country name equals to localname