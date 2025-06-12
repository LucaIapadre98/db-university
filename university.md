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

SELECT 
  AVG(vote) AS vote_average,
  COUNT(vote) AS vote_count
  FROM exam_student
  WHERE exam_id = "1";

  Non sono per appello però...


4. Contare quanti corsi di laurea ci sono per ogni dipartimento

SELECT count( department_id) AS appartamento
 FROM university.degrees
 WHERE 
 department_id = "3"




1. Selezionare tutti gli studenti iscritti al Corso di Laurea in Economia


2. Selezionare tutti i Corsi di Laurea Magistrale del Dipartimento di
Neuroscienze



3. Selezionare tutti i corsi in cui insegna Fulvio Amato (id=44)


4. Selezionare tutti gli studenti con i dati relativi al corso di laurea a cui
sono iscritti e il relativo dipartimento, in ordine alfabetico per cognome e
nome


5. Selezionare tutti i corsi di laurea con i relativi corsi e insegnanti


6. Selezionare tutti i docenti che insegnano nel Dipartimento di
Matematica (54)


7. BONUS: Selezionare per ogni studente il numero di tentativi sostenuti
per ogni esame, stampando anche il voto massimo. Successivamente,
filtrare i tentativi con voto minimo 18.