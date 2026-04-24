# Esercizio 

1. Contare quanti iscritti ci sono stati ogni anno
2. Contare gli insegnanti che hanno l'ufficio nello stesso edificio
3. Calcolare la media dei voti di ogni appello d'esame
4. Contare quanti corsi di laurea ci sono per ogni dipartimento


# Risultato

1.
SELECT count(enrolment_date) AS qtà_iscritti, year(enrolment_date) 
FROM students GROUP BY YEAR(enrolment_date);

2.
SELECT teachers.office_address, count(*) 
FROM teachers GROUP BY teachers.office_address

3.
SELECT exam_id AS id_appelli, 
ROUND(AVG(exam_student.vote), 2) AS media_voti 
FROM exam_student GROUP BY exam_student.exam_id

4.
SELECT departments.name, count(*) AS corsi_di_laurea 
FROM degrees JOIN departments ON departments.id = degrees.department_id GROUP BY department_id