# Week 4
## Exercise 5
### Question 1

select name from country
where iso_country in (select iso_country from airport where name like "Satsuma%");

![screenshot](ex5_q1.png)
### Question 2
select name from airport 
where iso_country in (select iso_country from airport where name like "Monaco%" );

![screenshot](ex5_q2.png)
### Question 3
select screen_name from game
where id in (select game_id from goal_reached 
where goal_id in (select id from goal where name="CLOUDS"));

![screenshot](ex5_q3.png)
### Question 4
select country.name from country
where iso_country not in (select airport.iso_country from airport);

![screenshot](ex5_q4.png)
### Question 5
select name from goal
where id not in (select goal.id from goal,goal_reached,game 
where game.id=game_id and goal.id=goal_id and screen_name="Heini");

![screenshot](ex5_q5.png)