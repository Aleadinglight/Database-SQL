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
sqlite> select name,population from country where population>5000000 and population<10000000;
```
18.Select the name and population of countries where the number of population is between 
5 and 10 million people that are in Europe ordered by population descending
```
sqlite> select name,population from country where population>5000000 and population<10000000 order by population desc;
```
19.Select the names of countries that start with A-letter but locate outside Europe
```
sqlite> select name from country where name like "A%" and continent!="Europe";
```
20.Select the name and population of the country that has most of population
```
sqlite> select name,MAX(population) from country;
```
21.Select the name and life expectancy of the country that has shortest life expectancy (not NULL one)
MIN() auto ignores NULL
```
sqlite> select name,MIN(lifeexpectancy) from country;
```
22.Count the total number of population in the table
```
sqlite> select SUM(population) from country;
```
23.Find all the Republic countries
```
sqlite> select name from country where governmentform="Republic";
```
24.Find countries who became independent after 1975
```
Vàng tâm mà ai khai khống, làm người yêu nước biểu tình bị dập
Mày nể ngoài đó 10 phần, nên thích thú nhìn đồng bào bị đập
Vinh quang thế đéo nào được, khi mày ăn cá của Formosa
Xài đồ giả của xứ La Phù, nhập tiền giả của bọn Trung Hoa
Đến cái tuyến metro của mày cũng là thằng Tàu thầu đểu﻿
Ngấu nghiến ăn cái màn thầu ai dè cái màn thầu yểu
Bốn ngàn năm văn hiến, chỉ hiến lũ cướp đói ăn...
sqlite> select name,indepyear from country where indepyear>1975 and indepyear is not null;
```
25.Find the ten oldest countries based on indepyear the name and year
```
sqlite> select name from country order by indepyear asc limit 10;
```
26.Select the current date and time
```
sqlite> select date('now'),time('now');
```
27.Find out what is the current year
```
sqlite> select strftime('%Y','now');
```
28.Calculate how old is the oldest existing country (UK)
```
sqlite> select name,cast(strftime('%Y','now') as decimal)-indepyear from country order by indepyear limit 1;
```
29.Calculate how old will Finland be this year
```
sqlite> select name,cast(strftime('%Y','now') as decimal)-indepyear from country where name="Finland";
```
30.Find out how many countries there is where the country name equals to localname
```
sqlite> select count(name) from country where name=localname;
```