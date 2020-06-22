About DB 
======

### 1. Find out when a particular table was created (in **`dba_objects`** table)
```sql
SELECT created
	FROM dba_objects
	WHERE object_name = <<your table name>>
		AND owner = <<owner of the table>>
		AND object_type = 'TABLE'
```

### 2. `ROWNUM` as a pseudocolumn and will be assigned the numbers 1, 2, 3, 4, ... N.

**A ROWNUM value is assigned to a row after it passes the predicate phase of the query but **before the query does any sorting or aggregation**.**

This query won't get any results:
```sql
SELECT * FROM employee where rownum > 1;
```

To get the Top N results from table:

```sql
/* this will get random 5 results with ignoring `order by`*/
select * from emp where ROWNUM <= 5 order by sal desc;

/*this is the correct way of top N query*/
SELECT * FROM (SELECT * FROM employee order by sal desc) where rownum <= 5;
```

### 3. String literials `q!...!`,anything between `q!` and `!` can be treated as text
```sql
declare
    v_num number(10) := &input_number;
    v_text varchar(40);
begin
    if v_num > 300 then
        v_text := q'!string literial i's text.!';
        dbms_output.put_line(v_text);
    end if;
end;
```
