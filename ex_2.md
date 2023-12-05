# JOIN

## 1

SELECT * FROM `students`
INNER JOIN `degrees` ON `degrees`.`id` = `students`.`degree_id`
WHERE `degrees`.`name` = 'Corso di Laurea in Economia';

## 2

SELECT * FROM `degrees`
INNER JOIN `departments` ON `departments`.`id` = `degrees`.`department_id`
WHERE `departments`.`name` = 'Dipartimento di Neuroscienze'
AND `degrees`.`level` = 'Magistrale';

## 3

SELECT * FROM `courses`
INNER JOIN `course_teacher` ON `course_teacher`.`teacher_id` = `courses`.`id`
INNER JOIN `teachers` ON `teachers`.`id` = `courses`.`id`
WHERE `teachers`.`name` = 'Fulvio' AND `teachers`.`surname` = 'Amato';

## 4

SELECT * FROM `students`
INNER JOIN `degrees` ON `degrees`.`id` = `students`.`degree_id`
INNER JOIN `departments` ON `departments`.`id` = `degrees`.`department_id`
ORDER BY `students`.`surname`, `students`.`name` ASC;

## 5

SELECT * FROM `degrees`
INNER JOIN `courses` ON `courses`.`id` = `degrees`.`id`
INNER JOIN `course_teacher` ON `course_teacher`.`teacher_id` = `courses`.`id`
INNER JOIN `teachers` ON `teachers`.`id` = `courses`.`id`;

## 6

SELECT * FROM `departments`
INNER JOIN `degrees` ON `degrees`.`id`
INNER JOIN `courses` ON `courses`.`id`
INNER JOIN `course_teacher` ON `course_teacher`.`teacher_id`
INNER JOIN `teachers` ON `teachers`.`id`
WHERE `departments`.`name` = 'Dipartimento di Matematica';