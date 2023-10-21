**Schema (MySQL v8.0)**

    CREATE TABLE students(
      first_name VARCHAR(30) NOT NULL,
      last_name VARCHAR(30) NOT NULL,
      email VARCHAR(60) NULL,
      street VARCHAR(50) NOT NULL,
      city VARCHAR(40) NOT NULL,
      state CHAR(2) NOT NULL DEFAULT "PA",
      zip MEDIUMINT UNSIGNED NOT NULL,
      phone VARCHAR(20) NOT NULL,
      birth_date DATE NOt NUll,
      sex ENUM('M', 'F') NOT NULL,
      date_entered TIMESTAMP,
      lunch_cost FLOAT NULL,
      student_id INT UNSIGNED NOT NULL AUTO_INCREMENT PRIMARY KEY
      );

---

**Query #1**

    INSERT INTO students (first_name, last_name, email, street, city, state, zip, phone, birth_date, sex, date_entered, lunch_cost)
    VALUES 
    ('Gift', 'Amachree', 'amacgift5@gmail.com', 'Kudirat', 'Ikeja', 'Ls', 1201001, '09082730273', '2020-08-17', 'F', NOW(), 3.50),
    ('John', 'Doe', 'john.doe@example.com', '123 Elm St', 'Anytown', 'PA', 12345, '123-456-7890', '2000-01-01', 'M', NOW(), 5.50),
    ('Jane', 'Smith', 'jane.smith@example.com', '456 Oak St', 'Somewhere', 'PA', 23456, '123-456-7891', '2001-02-02', 'F', NOW(), 6.00),
    ('Alice', 'Johnson', 'alice.johnson@example.com', '789 Pine St', 'Here', 'PA', 34567, '123-456-7892', '2002-03-03', 'F', NOW(), 5.75),
    ('Bob', 'Williams', 'bob.williams@example.com', '101 Maple St', 'There', 'PA', 45678, '123-456-7893', '2003-04-04', 'M', NOW(), 6.25),
    ('Charlie', 'Jones', 'charlie.jones@example.com', '202 Cedar St', 'Everywhere', 'PA', 56789, '123-456-7894', '2004-05-05', 'M', NOW(), 5.80),
    ('Debbie', 'Davis', 'debbie.davis@example.com', '303 Redwood St', 'Anywhere', 'PA', 67890, '123-456-7895', '2005-06-06', 'F', NOW(), 6.15),
    ('Eddie', 'Miller', 'eddie.miller@example.com', '404 Spruce St', 'Nowhere', 'PA', 78901, '123-456-7896', '2006-07-07', 'M', NOW(), 5.90),
    ('Faye', 'Wilson', 'faye.wilson@example.com', '505 Birch St', 'Someplace', 'PA', 89012, '123-456-7897', '2007-08-08', 'F', NOW(), 6.10),
    ('George', 'Taylor', 'george.taylor@example.com', '606 Cherry St', 'Elsewhere', 'PA', 90123, '123-456-7898', '2008-09-09', 'M', NOW(), 5.85),
    ('Holly', 'Moore', 'holly.moore@example.com', '707 Dogwood St', 'Yonder', 'PA', 12345, '123-456-7899', '2009-10-10', 'F', NOW(), 6.05)
    ;

There are no results to be displayed.

---
**Query #2**

    SELECT * FROM students;

| first_name | last_name | email                     | street         | city       | state | zip     | phone        | birth_date | sex | date_entered        | lunch_cost | student_id |
| ---------- | --------- | ------------------------- | -------------- | ---------- | ----- | ------- | ------------ | ---------- | --- | ------------------- | ---------- | ---------- |
| Gift       | Amachree  | <amacgift5@gmail.com>       | Kudirat        | Ikeja      | Ls    | 1201001 | 09082730273  | 2020-08-17 | F   | 2023-10-19 19:19:25 | 3.5        | 1          |
| John       | Doe       | <john.doe@example.com>      | 123 Elm St     | Anytown    | PA    | 12345   | 123-456-7890 | 2000-01-01 | M   | 2023-10-19 19:19:25 | 5.5        | 2          |
| Jane       | Smith     | <jane.smith@example.com>    | 456 Oak St     | Somewhere  | PA    | 23456   | 123-456-7891 | 2001-02-02 | F   | 2023-10-19 19:19:25 | 6          | 3          |
| Alice      | Johnson   | <alice.johnson@example.com> | 789 Pine St    | Here       | PA    | 34567   | 123-456-7892 | 2002-03-03 | F   | 2023-10-19 19:19:25 | 5.75       | 4          |
| Bob        | Williams  | <bob.williams@example.com>  | 101 Maple St   | There      | PA    | 45678   | 123-456-7893 | 2003-04-04 | M   | 2023-10-19 19:19:25 | 6.25       | 5          |
| Charlie    | Jones     | <charlie.jones@example.com> | 202 Cedar St   | Everywhere | PA    | 56789   | 123-456-7894 | 2004-05-05 | M   | 2023-10-19 19:19:25 | 5.8        | 6          |
| Debbie     | Davis     | <debbie.davis@example.com>  | 303 Redwood St | Anywhere   | PA    | 67890   | 123-456-7895 | 2005-06-06 | F   | 2023-10-19 19:19:25 | 6.15       | 7          |
| Eddie      | Miller    | <eddie.miller@example.com>  | 404 Spruce St  | Nowhere    | PA    | 78901   | 123-456-7896 | 2006-07-07 | M   | 2023-10-19 19:19:25 | 5.9        | 8          |
| Faye       | Wilson    | <faye.wilson@example.com>   | 505 Birch St   | Someplace  | PA    | 89012   | 123-456-7897 | 2007-08-08 | F   | 2023-10-19 19:19:25 | 6.1        | 9          |
| George     | Taylor    | <george.taylor@example.com> | 606 Cherry St  | Elsewhere  | PA    | 90123   | 123-456-7898 | 2008-09-09 | M   | 2023-10-19 19:19:25 | 5.85       | 10         |
| Holly      | Moore     | <holly.moore@example.com>   | 707 Dogwood St | Yonder     | PA    | 12345   | 123-456-7899 | 2009-10-10 | F   | 2023-10-19 19:19:25 | 6.05       | 11         |

---

[View on DB Fiddle](https://www.db-fiddle.com/f/7485kscpgGWVxzqbALasDW/0)
