# Week 4
## Exercise 4
### Question 1

select country.name as "country name", airport.name as "airport name"
from country
inner join airport on airport.iso_country= country.iso_country where country.name="Finland"
and airport.scheduled_service="yes";

![screenshot](ex4_q1.png)
### Question 2
select screen_name, airport.name from game
inner join airport on ident=location;

![screenshot](ex4_q2.png)
### Question 3
select screen_name, country.name 
from game inner join airport on ident=location
inner join country on country.iso_country=airport.iso_country;

![screenshot](ex4_q3.png)
### Question 4
select airport.name, screen_name
from airport
left join game on ident=location where name like "%Hels%";

![screenshot](ex4_q4.png)
### Question 5
select name, screen_name
from goal
left join goal_reached on goal.id=goal_id
left join game on game.id=game_id;

![screenshot](ex4_q5.png)