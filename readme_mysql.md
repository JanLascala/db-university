"step 0"

USE `university_data`;

-press lightning

"step 1" 
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

"step 2" 
Selezionare tutti i corsi che valgono più di 10 crediti (479)

SELECT * 
FROM `courses`
WHERE `cfu` > '10';

result 479 rows
3	45	16:05:58	SELECT * 
 FROM `courses`
 WHERE `cfu` > '10'
 LIMIT 0, 1000	479 row(s) returned	0.000 sec / 0.000 sec

"step 3" 

Selezionare tutti gli studenti che hanno più di 30 anni

SELECT * 
FROM `students`
WHERE YEAR(date_of_birth) BETWEEN 1900 AND 1995;  tried 1994 

result 1000
3	47	16:21:30	SELECT * 
 FROM `students`
 WHERE YEAR(date_of_birth) BETWEEN 1900 AND 1995
 LIMIT 0, 1000	1000 row(s) returned	0.000 sec / 0.000 sec

 "step 4"

 Selezionare tutti i corsi del primo semestre del primo anno di un qualsiasi corso di laurea (286)

 SELECT * 
FROM `courses`
WHERE `period`= "I semestre" AND `year`= "1";

3	50	16:28:50	SELECT * 
 FROM `courses`
 WHERE `period`= "I semestre" AND `year`= "1"
 LIMIT 0, 1000	286 row(s) returned	0.000 sec / 0.000 sec

" step 5"
Selezionare tutti gli appelli d'esame che avvengono nel pomeriggio (dopo le 14) del 20/06/2020 (21)

SELECT * 
FROM `exams`
WHERE `hour` > "14:00:00" AND `date` = "2020/06/20";

3	53	16:35:33	SELECT * 
 FROM `exams`
 WHERE `hour` > "14:00:00" AND `date` = "2020/06/20"
 LIMIT 0, 1000	21 row(s) returned	0.031 sec / 0.000 sec

" step 6"
Selezionare tutti i corsi di laurea magistrale (38)

SELECT * 
FROM `degrees`
WHERE `level`= "magistrale";

3	56	16:38:00	SELECT * 
 FROM `degrees`
 WHERE `level`= "magistrale"
 LIMIT 0, 1000	38 row(s) returned	0.000 sec / 0.000 sec

 
 
"step 7"
Da quanti dipartimenti è composta l'università? (12)

SELECT * 
FROM `departments`

3	57	16:39:18	SELECT * 
 FROM `departments`
 LIMIT 0, 1000	12 row(s) returned	0.016 sec / 0.000 sec

"step 8"

Quanti sono gli insegnanti che non hanno un numero di telefono? (50)

SELECT * 
FROM `teachers`
WHERE `phone` IS NULL;

3	62	16:43:05	SELECT * 
 FROM `teachers`
 WHERE `phone` IS NULL
 LIMIT 0, 1000	50 row(s) returned	0.000 sec / 0.000 sec
