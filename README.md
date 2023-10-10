# Educational Institution Management System.

Here's the ER diagram description modified to use "institutions" instead of "schools." This
description includes entities, relationships, attributes, and cardinalates for a multi-institution student
management system.

## Entities:

### 1. Institution 
- Attributes: Institution ID (Primary Key), Institution Name, Address, Contact Details

### 2. Student 
- Attributes: Student ID (Primary Key), First Name, Last Name, Date of Birth, Contact Details 
- Relationships: Many-to-One with Institution, One-to-Many with Parent/Guardian, One-to-Many
with Enrollment

### 3. Parent/Guardian
- Attributes: Guardian ID (Primary Key), First Name, Last Name, Relationship to Student,
Contact Details
- Relationships: One-to-Many with Student

### 4. Class/Grade
- Attributes: Class ID (Primary Key), Class Name
- Relationships: Many-to-One with Institution, One-to-Many with Enrollment

### 5. Teacher
- Attributes: Teacher ID (Primary Key), First Name, Last Name, Subject Specialization, Contact
Details
- Relationships: Many-to-One with Institution, One-to-Many with Teaching Assignment

### 6. Course/Subject
- Attributes: Course ID (Primary Key), Course Name, Description

### 7. Enrollment
- Attributes: Enrollment ID (Primary Key), Enrollment Date
- Relationships: Many-to-One with Student, Many-to-One with Class

### 8. Teaching Assignment
- Attributes: Assignment ID (Primary Key)
- Relationships: Many-to-One with Teacher, Many-to-One with Course

## Relationships:

### 1. Student-Parent Relationship
- One-to-Many relationship between Student and Parent/Guardian.

### 2. Enrollment-Student Relationship
- One-to-Many relationship between Enrollment and Student.