# Week 3
## Exercise 3
### Question 1
	
select country.name as "country name", airport.name as "airport name"
from airport, country
where airport.iso_country = country.iso_country and country.name = "Iceland";

![screenshot](ex3_q1.png)
### Question 2
select name as "airport name" from airport where iso_country="FR" and type="large_airport";

![screenshot](ex3_q2.png)
### Question 3
select (select name from country where continent="AN") 
as "country name", name as "airport name" 
from airport where continent="AN";

![screenshot](ex3_q3.png)
### Question 4
select elevation_ft
from airport, game
where airport.id=game.id and
game.screen_name="Heini"

![screenshot](ex3_q4.png)
### Question 5
select elevation_ft*0.3048 as elevation_m
from airport, game
where airport.id=game.id and
game.screen_name="Heini";

![screenshot](ex3_q5.png)
### Question 6
select name
from airport, game
where location=ident and screen_name="Ilkka";

![screenshot](ex3_q6.png)
### Question 7
select country.name
from country, airport, game
where game.location=airport.ident and
airport.iso_country=country.iso_country and
game.screen_name="Ilkka";

![screenshot](ex3_q7.png)
### Question 8
select goal.name
from goal, goal_reached,game 
where goal.id=goal_reached.goal_id and
game.id=goal_reached.game_id and
game.screen_name="Heini";

![screenshot](ex3_q8.png)
### Question 9
select airport.name
from airport,goal,goal_reached,game 
where ident=location and
game.id=goal_reached.game_id and 
goal.id=goal_reached.goal_id and 
game.screen_name="Ilkka";

![screenshot](ex3_q9.png)
### Question 10
select country.name
from country,airport,goal,goal_reached,game 
where airport.iso_country=country.iso_country and
airport.ident=game.location and
game.id=goal_reached.game_id and 
goal.id=goal_reached.goal_id and 
game.screen_name="Ilkka";

![screenshot](ex3_q10.png)