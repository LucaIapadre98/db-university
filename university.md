1. Selezionare tutti gli studenti nati nel 1990 (160)

SELECT count(*)
FROM students
WHERE YEAR(date_of_birth) = "1990"

2. Selezionare tutti i corsi che valgono più di 10 crediti (479)

SELECT count(*)
FROM courses
WHERE cfu > 10 

3. Selezionare tutti gli studenti che hanno più di 30 anni

SELECT * 
FROM students
WHERE date_of_birth < "1995-01-01"

4. Selezionare tutti i corsi del primo semestre del primo anno di un qualsiasi corso di
laurea (286)

SELECT count(*) 
FROM courses
WHERE period = "I semestre" 
AND year= "1"


5. Selezionare tutti gli appelli d'esame che avvengono nel pomeriggio (dopo le 14) del
20/06/2020 (21)

SELECT count(*) 
FROM  exams
WHERE 
hour >= "14:00:00" 
AND  date= "2020-06-20"


6. Selezionare tutti i corsi di laurea magistrale (38)

SELECT count(*)
 FROM degrees
 WHERE 
 level= "magistrale"

7. Da quanti dipartimenti è composta l'università? (12)

SELECT count(*)
 FROM departments;

8. Quanti sono gli insegnanti che non hanno un numero di telefono? (50)

SELECT count(*)
 FROM teachers
 WHERE
 phone IS NOT NULL


1. Contare quanti iscritti ci sono stati ogni anno

SELECT count(*)
 FROM students
 WHERE
   enrolment_date >= "2020-01-01" AND
   enrolment_date <= "2020-12-31";

   oppure:

SELECT count(*)
 FROM students
 WHERE
   enrolment_date BETWEEN "2020-01-01" AND "2020-12-31";

Nel 2020 ci sono 1645 iscritti


2. Contare gli insegnanti che hanno l'ufficio nello stesso edificio


3. Calcolare la media dei voti di ogni appello d'esame


4. Contare quanti corsi di laurea ci sono per ogni dipartimento