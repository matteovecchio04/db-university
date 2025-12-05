# Table_name: departmets
# Entity_name: department
id: BIGINT PRIMARY_KEY AUTO_INCREMENT UNSIGNED
name: VARCHAR(50) NOT_NULL

# Table_name: degrees
# Entity_name: degree
id: BIGINT PRIMARY_KEY AUTO_INCREMENT UNSIGNED
department_id: BIGINT FK UNSIGNED
name: VARCHAR(50) NOT_NULL

# Table_name: courses
# Entity_name: course
id: BIGINT PRIMARY_KEY AUTO_INCREMENT UNSIGNED
degree_id: BIGINT FK UNSIGNED
name: VARCHAR(50) NOT_NULL

# Table_name: teachers
# Entity_name: teacher
id: BIGINT PRIMARY_KEY AUTO_INCREMENT UNSIGNED
course_id: BIGINT FK UNSIGNED
name: VARCHAR(50) NOT_NULL

# Table_name: exams
# Entity_name: exam
id: BIGINT PRIMARY_KEY AUTO_INCREMENT UNSIGNED
course_id: BIGINT FK UNSIGNED
name: VARCHAR(50) NOT_NULL

# Table_name: students
# Entity_name: student
id: BIGINT PRIMARY_KEY AUTO_INCREMENT UNSIGNED
degree_id: BIGINT FK UNSIGNED
name: VARCHAR(50) NOT_NULL

# Pivot_table: exam_student
student_id: BIGINT FK UNSIGNED
exam_id: BIGINT FK UNSIGNED
vote: TINYINT NOT_NULL

