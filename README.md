# 📘 SQL Internship - Task 4: Aggregate Functions and Grouping

## 🧠 Objective:
To use **aggregate functions** (`SUM`, `COUNT`, `AVG`) and **grouping techniques** (`GROUP BY`, `HAVING`) to summarize and analyze tabular data effectively.

---

## 🛠️ Tools Used:
- **DB Browser for SQLite** / **MySQL Workbench**
- **SQL Language** (MySQL dialect used)

---

## 🗂️ Dataset:
This task uses a database called `LibraryDB`, which includes the following tables:

- **Authors**: Contains `AuthorID`, `Name`
- **Books**: Contains `BookID`, `Title`, `AuthorID`
- **Members**: Contains `MemberID`, `Name`, `Email`
- **Loans**: Contains `LoanID`, `BookID`, `MemberID`, `LoanDate`, `ReturnDate`

---

## 📊 SQL Queries & Descriptions:

1. **Total Number of Books by Each Author**
```sql
SELECT a.Name AS AuthorName, COUNT(b.BookID) AS TotalBooks
FROM Authors a
JOIN Books b ON a.AuthorID = b.AuthorID
GROUP BY a.AuthorID;
# Task-4-Aggregate-Functions-and-Grouping
