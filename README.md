# College-Management-System-MySQL-
Concepts Used  Primary Key,  Foreign Key,  INNER JOIN,  Table Relationships,  Data Normalization.
SELECT 
    d.course_id,
    d.name AS department_name,
    t.name AS teacher_name
FROM departments d
JOIN teachers t ON d.course_id = t.course_id;
ALTER TABLE student
ADD course_id INT;

ALTER TABLE student
ADD CONSTRAINT fk_student_course
FOREIGN KEY (course_id) REFERENCES departments(course_id);
SELECT
    s.rollno,
    s.name AS student_name,
    d.name AS department_name,
    t.name AS teacher_name
FROM student s
JOIN departments d ON s.course_id = d.course_id
JOIN teachers t ON d.course_id = t.course_id;
SELECT
    s.rollno,
    s.name AS student_name,
    d.name AS department_name,
    t.name AS teacher_name
FROM student s
JOIN departments d ON s.course_id = d.course_id
JOIN teachers t ON d.course_id = t.course_id;
