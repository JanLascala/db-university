// 1 Selezionare tutti gli studenti iscritti al Corso di Laurea in Economia

-- SELECT *
FROM `students` 
JOIN  `degrees` ON `degree_id`=`degrees`.`id`
WHERE `degrees`.`name` = 'Corso di Laurea in Economia';

-- result = 68 rows.

// 2 Selezionare tutti i Corsi di Laurea Magistrale del Dipartimento di Neuroscienze

-- SELECT *
FROM `courses` 
JOIN  `degrees` ON `degree_id`=`degrees`.`id`
JOIN `departments` ON `department_id`= `departments`.`id`
WHERE `degrees`.`level` = 'magistrale' AND `departments`.`name` = 'Dipartimento di Neuroscienze';

-- result = 18 rows

// 3 Selezionare tutti i corsi in cui insegna Fulvio Amato (id=44)

-- SELECT * 
FROM `courses` 
JOIN `course_teacher` ON `courses`.`id` = `course_teacher`.`course_id`
WHERE `course_teacher`.`teacher_id`= 44

-- result = 11 rows

//4 Selezionare tutti gli studenti con i dati relativi al corso di laurea a cui sono iscritti
e il relativo dipartimento, in ordine alfabetico per cognome e nome

--SELECT * 
FROM `students` 
JOIN `degrees` ON `degrees`.`id`= `degree_id`
JOIN `courses` ON `courses`.`degree_id` = `degrees`.`id`
JOIN `departments` ON `departments`.`id`= `department_id`
ORDER BY `students`.`name`, `students`.`surname` ASC;

--result= 1000 rows

//5 Selezionare tutti i corsi di laurea con i relativi corsi e insegnanti

-- SELECT * 
FROM `courses`
JOIN `degrees` ON `degrees`.`id`= `degree_id`
JOIN `course_teacher` ON `courses`.`id` = `course_teacher`.`course_id`
JOIN `teachers`ON `teachers`.`id`= `teacher_id`; 

--result= 1000 rows

//6 Selezionare tutti i docenti che insegnano nel Dipartimento di Matematica (54)

-- SELECT  DISTINCT `teachers`.`name`,`teachers`.`surname`, `departments`.`name`
FROM `teachers`
JOIN `course_teacher` ON `teachers`.`id` =`teacher_id`
JOIN `courses`ON `courses`.`id`= `course_id`
JOIN `degrees` ON `degrees`.`id`= `degree_id`
JOIN `departments` ON `departments`.`id`= `department_id`
WHERE `departments`.`name` = 'Dipartimento di Matematica';

--result= 54 

// GROUP 

// 1 Contare quanti iscritti ci sono stati ogni anno

--SELECT `enrolment_date`, COUNT(*) AS `student_count`
FROM `students`
GROUP BY `enrolment_date`;

// 2 Contare gli insegnanti che hanno l'ufficio nello stesso edificio

--SELECT `teachers`.`office_address`, COUNT(*)
FROM `teachers`
GROUP BY `office_address`;

//3 Calcolare la media dei voti di ogni appello d'esame


//4 Contare quanti corsi di laurea ci sono per ogni dipartimento

--SELECT `departments`.`name`, COUNT(`degrees`.`name`)
FROM `degrees`
JOIN `departments` ON `degrees`.`department_id`= `departments`.`id`
GROUP BY `departments`.`name`;