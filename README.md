![kirstenmarie-Dtim0H8G1Ws-unsplash](https://github.com/user-attachments/assets/f423ec9c-9199-40fd-af43-97b5fed17003)



# Student Management System (SMS) Database

## Project Overview
The **Student Management System (SMS)** is a relational database designed to efficiently manage and organize information about students, departments, courses, instructors, and enrollments within a university setting.  

The database was created in **PostgreSQL (pgAdmin)** and demonstrates how structured relationships and SQL queries can support key academic operations such as:
- Registering students and instructors  
- Assigning instructors to courses  
- Enrolling students in courses  
- Generating analytical and operational reports  

---

## Objectives
- Design and implement a relational database for university operations.  
- Ensure **data integrity, scalability, and efficient querying** using primary and foreign key constraints.  
- Enable reporting on student enrollment, course distribution, and instructor performance.  
- Demonstrate the use of SQL joins, aggregations, and conditions to generate meaningful insights.

---

## Entity Relationship Diagram (ERD)
<img width="1493" height="810" alt="Student Management System Diagram" src="https://github.com/user-attachments/assets/cec41e59-b982-446a-94ed-f45b04e5ec90" />

---

## Database Structure

The SMS database is built on six relational tables linked by **primary and foreign key constraints**.

| Table | Description |
|--------|-------------|
| `Students` | Stores student personal and academic details. |
| `Departments` | Contains information about the university’s departments. |
| `Courses` | Defines courses offered by departments. |
| `Instructors` | Stores instructor details and their affiliated department. |
| `Enrollments` | Tracks student registrations in courses. |
| `CourseInstructors` | Establishes the many-to-many relationship between courses and instructors. |

### Relationships
- One Department → Many Students, Courses, and Instructors  
- One Student → Many Enrollments  
- One Course → Many Enrollments  
- One Instructor → Many Course Assignments  
- Courses and Instructors → Many-to-Many via `CourseInstructors`

---

## Data Population
The tables were populated with realistic sample data representing a mid-sized university:
- **6 Departments**
- **20 Courses**
- **15 Instructors**
- **50 Students**
- **100 Enrollment Records**
- **28 Course Assignments**

---

## Analytical SQL Queries

| Query Objective | SQL Logic Summary |
|-----------------|------------------|
| **Total Students per Course** | Counts enrollments grouped by course name. |
| **Students Enrolled in Multiple Courses** | Uses `HAVING COUNT(*) > 1` to filter multi-course enrollments. |
| **Students per Department** | Aggregates student count per department. |
| **Average Courses per Student** | Calculates the mean number of courses per student. |
| **Gender Distribution** | Joins student, course, and instructor tables to analyze gender distribution across courses. |

---

## Key Insights
1. **Enrollment Distribution:**  
   - *Introduction to Programming (CS001)*, *Data Structures (CS002)*, and *Linear Algebra (CS009)* had the highest enrollments (7 students each).  
   - *Academic Writing (CS019)* recorded the lowest (3 students).

2. **Departmental Distribution:**  
   - *Computer Science* department had the highest student population (12).  
   - *Physics* and *Biology* had the least (7 students each).

3. **Course-Instructor Insights:**  
   - *Dr. Samuel Okoro* and *Dr. Samuel Kuti* taught the most male students (*Data Structures*).  
   - *Mr. Daniel Peters* taught the most female students (*Linear Algebra*).  
   - Each student enrolled in an average of **two courses**.

---

## Tools & Technologies
- **Database Management:** PostgreSQL (pgAdmin)  
- **Language:** SQL (DDL & DML)  
- **Environment:** Visual Studio Code / pgAdmin Query Tool  
- **Skills Demonstrated:** Database Design, ERD Modeling, SQL Joins, Aggregations, Grouping, and Reporting  

---

## Conclusion
The **Student Management System (SMS)** demonstrates how a well-structured relational database can streamline academic record management.  
It highlights:
- Data integrity through relational constraints  
- Flexibility for advanced analytical reporting  
- Scalability for larger institutional datasets  

This project reflects applied understanding of relational database design, SQL reporting, and data-driven decision support within an academic context.

---

### Acknowledgment
Originally completed as part of a collaborative team project.  
*Database design, SQL implementation, and analysis by LearnWithWida Intermediate Team B*  
