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