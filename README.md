SELECT * FROM Student;

SELECT Surname, tel FROM Student;

SELECT * FROM Student WHERE tel IS NULL;

SELECT Surname, Subject, Mark FROM StudentMarks;

SELECT Surname FROM StudentMarks WHERE Subject = 'Математика' AND Mark = 2;

SELECT CONCAT(Surname, ' ', LEFT(Name, 1)) 

FROM Student 

WHERE Surname LIKE 'а%' AND Surname LIKE '%в%';

SELECT Surname, tel 

FROM Student 

WHERE tel REGEXP '^[2-5,7]+$';

SELECT Surname FROM Student WHERE address LIKE '%д.78%';

SELECT * FROM Student WHERE Surname IN ('Иванов', 'Петров', 'Сидоров');

SELECT Surname FROM Student 

WHERE Surname BETWEEN 'Иванов' AND 'Сидоров' 

ORDER BY Surname;

SELECT DISTINCT Surname

FROM StudentMarks 

WHERE Subject = 'Математика' AND Mark >= 3;

SELECT DISTINCT Mark, (Mark * 20) AS Mark_100 

FROM StudentMarks;

