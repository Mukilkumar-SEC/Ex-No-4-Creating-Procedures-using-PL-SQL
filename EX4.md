# Ex. No: 4 Creating Procedures using PL/SQL
##DATE: 
### AIM: 
To create a procedure using PL/SQL.

### Steps:
1. Create employee table with following attributes (empid NUMBER, empname VARCHAR(10), dept VARCHAR(10),salary NUMBER);
2. Create a procedure named as insert_employee data.
3. Inside the procdure block, write the query for inserting the values into the employee table.
4. End the procedure.
5. Call the insert_employee data procedure to insert the values into the employee table.
6. Display the employee table

### Program:
```
CREATE TABLE exp4(
       regno NUMBER,
       USERNAME VARCHAR(10),
       DEPT VARCHAR(10),
       MARKS NUMBER
       );
       CREATE OR REPLACE PROCEDURE exp4_data AS
    BEGIN
    INSERT INTO exp4(regno,USERNAME,DEPT,MARKS)
    values(1,'MUKESH','AIDS',50);
    INSERT INTO exp4(regno,USERNAME,DEPT,MARKS)
    values(2,'SAKTHI','AIDS',75);
    INSERT INTO exp4(regno,USERNAME,DEPT,MARKS)
    values(3,'SHREE','CSE',99);
    COMMIT;
   FOR exp4_rec IN (SELECT * FROM exp4)LOOP
   DBMS_OUTPUT.PUT_LINE('STUDENT ID:'||exp4_rec.regno||',STUDENT NAME:'|| exp4_rec.USERNAME||
   ',DEPARTMENT:'||exp4_rec.DEPT||',MARK:'||exp4_rec.MARKS);
   END LOOP;
   END;
  /
```

### Output:
![Screenshot 2023-10-06 161318](https://github.com/Mukilkumar-SEC/Ex-No-4-Creating-Procedures-using-PL-SQL/assets/119559663/b397fe74-6b3f-4b32-88b5-27f53e1bbe99)

### Result:
Thus,the output has been succesfully verified.
