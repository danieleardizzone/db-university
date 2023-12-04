# db-university query

## 1

SELECT *
FROM `students`
WHERE `date_of_birth` LIKE '1990-%';

## 2

SELECT * 
FROM `courses`
WHERE `cfu` > '10';

## 3

## 4

SELECT * FROM `courses`
WHERE `year` = '1'  AND `period` = 'I semestre';

## 5

SELECT * FROM `exams`
WHERE `date` = '2020-06-20' AND `hour` >= '14:00:00';

## 6

SELECT * FROM `degrees`
WHERE `level` = 'magistrale';

## 7

SELECT MAX(id) AS number_of_departments
FROM `departments`;

## 8

SELECT * 
FROM `teachers`
WHERE `phone` IS NULL;