Oracle basics
========

### 1. `Constant` and `Not null`
```sql
	
	DECLARE
		v_variable1 number(10) not null := 10;
		v_variable2 number(10) DEFAULT 10;
		v_variable3 CONSTANT number(10) := 1000;

```


### 2. **`%TYPE`**
	```sql
		DECLARE
			v_salary employee.salary%TYPE; -- reference a field row type
			v_mySalary v_salary%TYPE;	-- use on a variable type
	```

### 3. **`%ROWTYPE`** is a type of record which reference a identified field from table, doesn't need to declare whole table data types.


```sql
	DECLARE	
		v_rowEmp Employee%ROWTYPE;
	BEGIN
		select l_name,age into v_rowEmp.lname, v_rowEmp.age from Employee;
	END;
```


### 4. **Declare the user defined record**
```sql
	DECLARE
	--Simple type declaration
	  TYPE BonusCompensation
	    IS RECORD (CashPayment    NUMBER(6),
	               CompanyCar     BOOLEAN,
	               VacationWeeks  NUMBER(2)
	               );
	  
	  --Extended type declaration
	  TYPE EmpRecord
	    IS RECORD (ssn            employee.ssn%TYPE,
	               LName          employee.lname%TYPE,
	               DName          department.DName%TYPE,
	               BonusPayment   BonusCompensation
	               );
	               
	  --Another extended type declaration along with the instance declaration
	  TYPE ManagerRecord
	    IS RECORD (ssn            employee.ssn%TYPE,
	               BonusPayment   BonusCompensation
	               );
	               
	  --Instance Declaration
	  BestEmp       EmpRecord;
	  BestManager   ManagerRecord;

	BEGIN
		/* logic goes here...*/
	END;

```

### 5.**date** data type stored as numeric value in database
	to get 100 days after today just add 100 behind
```sql
	BEGIN
		dbms_output.put_line(sysdate + 100);
	end;
```





