sqlite> .tables

1.Select all the countries
```
sqlite> .schema country
select * from country;
```
2.Select just all the country names 
`select "name" from country;`

select name and capital of all the countries
select just all the country names in descending mode (last alphabets first)
select just all the country names just for five first countries
select just all the country names just for 100 first countries
select just all the country names but order the result by the country name
select name of the countries where the name has 'ia'
select region and the country names but order the result initially by the region and then by the country name
select the country names ordered by the population, the biggest countries first
select the name and the region of all the countries
find countries with the name starting with Y-letter
find continent and name of countries where the continent is Europe
find continent and name of countries  where the continent is Europe or Asia
find region, name and population of the first biggest European counties by size
select the name and life expectancy of countries where life expectancy is more than 80
select the name and population of countries where the number of population is between 5 and 10 million people
select the name and population of countries where the number of population is between 5 and 10 million people that are in Europe ordered by population descending
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