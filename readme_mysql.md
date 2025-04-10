"step 1"

USE `university_data`;

-press lightning

"step 2" 
Selezionare tutti gli studenti nati nel 1990 (160)

SELECT *  
FROM `students`;
all student selected

SELECT * 
FROM `students`
WHERE YEAR(date_of_birth) IN || = (1990);    (both IN and = work!)

result 160 rows
3	37	15:59:04	SELECT * 
 FROM `students`
 WHERE YEAR(date_of_birth) = (1990)
 LIMIT 0, 1000	160 row(s) returned	0.000 sec / 0.000 sec

"step 3" 
Selezionare tutti i corsi che valgono più di 10 crediti (479)

SELECT * 
FROM `courses`
WHERE `cfu` > '10';

result 479 rows
3	45	16:05:58	SELECT * 
 FROM `courses`
 WHERE `cfu` > '10'
 LIMIT 0, 1000	479 row(s) returned	0.000 sec / 0.000 sec

"step 4" 

Selezionare tutti gli studenti che hanno più di 30 anni

SELECT * 
FROM `students`
WHERE YEAR(date_of_birth) BETWEEN 1900 AND 1995;  tried 1994 

result 1000
3	47	16:21:30	SELECT * 
 FROM `students`
 WHERE YEAR(date_of_birth) BETWEEN 1900 AND 1995
 LIMIT 0, 1000	1000 row(s) returned	0.000 sec / 0.000 sec

 "step 5"

 Selezionare tutti i corsi del primo semestre del primo anno di un qualsiasi corso di laurea (286)

 SELECT * 
FROM `courses`
WHERE `period`= "I semestre" AND `year`= "1";

3	50	16:28:50	SELECT * 
 FROM `courses`
 WHERE `period`= "I semestre" AND `year`= "1"
 LIMIT 0, 1000	286 row(s) returned	0.000 sec / 0.000 sec

" step 6"


