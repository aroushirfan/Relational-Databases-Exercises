# Week 5
## Exercise 7
### Question 1
update game
set location= (select ident from airport where name = "Nottingham Airport"), 
co2_consumed= co2_consumed+500
where screen_name= "Vessa";

![screenshot](ex7_q1.png)
### Question 2


![screenshot](ex7_q2.png)
### Question 3
delete from goal_reached;
select*from goal_reached;

![screenshot](ex7_q3.png)
### Question 4
delete from game;
select*from game;

![screenshot](ex7_q4.png)