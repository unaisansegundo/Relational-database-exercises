# Student: Unai San Segundo (2417471)
# Week 2:
### Exercises 2:
#### Question 1:
select * from goal;
![](attachments/W2Q1.png)
![](attachments/W2Q1R.png)

#### Question 2:
select name, type from airport where iso_country = "FI";
![](attachments/W2Q2.png)
![](attachments/W2Q2R.png)

#### Question 3:
select name from airport where iso_country = 'FI' order by name ASC;
![](attachments/W2Q3.png)
![](attachments/W2Q3R.png)
#### Question 4:
select name, type from airport where iso_country = 'FI' order by type, name;
![](attachments/W2Q4.png)
![](attachments/W2Q4R.png)
#### Question 5:
select name from country where name like 'F%'
![](attachments/W2Q5.png)
![](attachments/W2Q5R.png)
#### Question 6:
select name from country where name LIKE '%f%'
![](attachments/W2Q6.png)
![](attachments/W2Q6R.png)
#### Question 7:\
select location from game where screen_name = 'Vesa';
![](attachments/W2Q7.png)
![](attachments/W2Q7R.png)
#### Question 8:
select co2_consumed from game where screen_name = 'Ilkka';
![](attachments/W2Q8.png)
![](attachments/W2Q8R.png)
#### Question 9:
select co2_budget from game limit 1;
![](attachments/W2Q9.png)
![](attachments/W2Q9R.png)
#### Question 10:
select screen_name,co2_budget,co2_consumed, co2_budget-co2_consumed AS co2left from game where screen_name = 'Ilkka';
![](attachments/W2Q10.png)

### Exercises 3:
#### Question 1:
select country.name as 'country name', airport.name as 'airport name'
from airport, country
where airport.iso_country = country.iso_country and airport.iso_country = 'IS';
![](attachments/W3Q1.png)
![](attachments/W3Q1R.png)
#### Question 2:
select airport.name as 'airport name'
from airport, country
where airport.iso_country = country.iso_country
and airport.iso_country = 'FR' and airport.type = 'large_airport';
![](attachments/W3Q2.png)
![](attachments/W3Q2R.png)
#### Question 3:
select country.name as 'country name', airport.name as 'airport name'
from airport, country 
where airport.iso_country = country.iso_country 
and airport.iso_country = 'AQ';
![](attachments/W3Q3.png)
![](attachments/W3Q3R.png)
#### Question 4:
select airport.elevation_ft
from airport, game
where airport.ident = game.location and game.screen_name = 'Heini';
![](attachments/W3Q4.png)
![](attachments/W3Q4R.png)
#### Question 5:
select airport.elevation_ft * 0.3048 as elevation_m
from airport, game
where airport.ident = game.location and game.screen_name = 'Heini';
![](attachments/W3Q5.png)
![](attachments/W3Q5R.png)
#### Question 6:
select airport.name
from airport, game
where airport.ident = game.location and game.screen_name = 'Ilkka';
![](attachments/W3Q6.png)
![](attachments/W3Q6R.png)
#### Question 7:
select country.name
from airport, game, country
where airport.ident = game.location and airport.iso_country = country.iso_country and game.screen_name = 'Ilkka';
![](attachments/W3Q7.png)
![](attachments/W3Q7R.png)
#### Question 8:
select goal.name
from goal_reached, game, goal
where goal.id = goal_reached.goal_id and goal_reached.game_id = game.id and game.screen_name = 'Heini';
![](attachments/W3Q8.png)
![](attachments/W3Q8R.png)
#### Question 9:
select airport.name
from goal_reached, game, goal, airport
where airport.ident = game.location and goal.id = goal_reached.goal_id and goal_reached.game_id = game.id 
and game.screen_name = 'Ilkka' and goal.name = 'CLOUDS';
![](attachments/W3Q9.png)
![](attachments/W3Q9R.png)
#### Question 10:
select country.name
from goal_reached, game, goal, airport, country
where airport.iso_country = country.iso_country and airport.ident = game.location 
and goal.id = goal_reached.goal_id and goal_reached.game_id = game.id 
and game.screen_name = 'Ilkka' and goal.name = 'CLOUDS';
![](attachments/W3Q10.png)
![](attachments/W3Q10R.png)

# Week 3:
### Exercises 4:
#### Question 1:
 select country.name, airport.name
from country inner join airport on airport.iso_country = country.iso_country
where airport.scheduled_service = 'yes' and country.name = 'Finland';
![](attachments/W4Q1.png)
![](attachments/W4Q1R.png)
#### Question 2:
select game.screen_name, airport.name
from game inner join airport on airport.ident = game.location;
![](attachments/W4Q2.png)
![](attachments/W4Q2R.png)
#### Question 3:
![](attachments/W4Q3.png)
![](attachments/W4Q3R.png)
#### Question 4:
select airport.name, game.screen_name
from airport left join game on airport.ident = game.location
where airport.name like '%Hels%'
![](attachments/W4Q4.png)
![](attachments/W4Q4R.png)
#### Question 5:
select goal.name, game.screen_name
from goal left join goal_reached on goal.id = goal_reached.goal_id
left join game on game.id = goal_reached.game_id;
![](attachments/W4Q5.png)
![](attachments/W4Q5R.png)