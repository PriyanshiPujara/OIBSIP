# Task 3 - SQL Injection on DVWA (Low Security)

## Objective
Demonstrate an SQL Injection vulnerability using Damn Vulnerable Web Application (DVWA) configured with Low Security.

## Tools Used
- DVWA (Damn Vulnerable Web Application)
- XAMPP
- MySQL
- PHP

## Environment Setup
1. Installed XAMPP.
2. Downloaded and configured DVWA.
3. Created the DVWA database in phpMyAdmin.
4. Configured the database connection.
5. Set DVWA Security Level to Low.

## Procedure
1. Logged into DVWA.
2. Set Security Level to Low.
3. Opened the SQL Injection module.
4. Submitted input to the vulnerable field.
5. Observed the application's response.

## Output

The application returned multiple user records from the database:

| First Name | Surname |
|------------|----------|
| admin | admin |
| Gordon | Brown |
| Hack | Me |
| Pablo | Picasso |
| Bob | Smith |

## Vulnerability Explanation

SQL Injection occurs when user input is directly incorporated into an SQL query without proper validation or parameterized queries.

In DVWA Low Security mode, the application intentionally lacks protections against SQL Injection. As a result, the database query returned multiple records instead of only the expected result.

## Impact

- Unauthorized access to database records
- Exposure of sensitive information
- Authentication bypass risks
- Potential data manipulation

## Prevention

- Prepared Statements
- Parameterized Queries
- Input Validation
- Least Privilege Principle
- Stored Procedures

## Conclusion

This task demonstrated how SQL Injection vulnerabilities can expose unintended database information when applications fail to properly validate user input.
