#T-SQL Fundamentals
- Server Character Set ISO 8859-1 (ANSI or Latin1)
- Identifier
- Batches (GO)
 - is a set of SQL and Transact-SQL satement submitted for execution as a group.
 - no nested allowed
- Variables @ @@
 - Declaration
  ```
  DECLARE {{@local_variable [AS] data_type}[=value]}[,....n]

  DECLARE @type int=10
  DECLARE @name verchar(50)

  DECLARE @type int=10, @name varchar(50)
  ```
 - Assignment
  ```
  SET {@local_variable=expression}|
      {@local_variable{+=|<=|*=}expression }
  ```

#Control-of-flow Language
- begin...end
- return
- break
- continue
- goto label
- while
- if...else
- case
```
case
  when then
end
```

#Cursor (select)
- DECLARE cursor_name [INSENSITIVE][SCROLL] CURSOR FOR select_statement
  [FOR {READONLY|UPDATE[OF column_name [,...n]]}]
- OPEN {cursor_name|cursor_variable_name}
- FETCH [ [NEXT|PRIOR|FIRST] FROM ] {{cursor_name}|@cursor_variable_name}
  [INTO variable_name[,...n]]
```
open @m_cur

close @m_cur
deallocate @m_cur
```

#Error Handling
- @@ERROR (0:success)
- Try...Catch
```
BEGIN TRY
  {...}
END TRY
BEGIN CATCH
  {...}
END CATCH
```

#Stored Procedure
- is a saved collection of Transact-SQL statements that can take and return 
  user-supplied parameters.
- it never returns value which is different from function
- Benefits
  - Speed
  - Code reuse and abstraction
  - Security
  - Reduced traffic between client and server
- Syntax
```
CREATE {PROC|PROCEDURE} [schema_name.]procedure_name 
       [{@parameter [type_schema_name.]data_type}
         [=default][OUT|OUTPUT][READONLY]
       ][,...n]
AS <sql_statement>
GO
```
```
CREATE PROCEDURE Example
    @emp_cur CURSOR VARYING OUTPUT
AS
    SET NOCOUNT ON
    SET @emp_cur=CURSOR FOR
          SELECT ...
    OPEN @emp_cur
GO
```

#Trigger (DML trigger)
- is a special kind of stored procedure that automatically executes when an
  even occurs
- Syntax
```
CREATE TRIGGER [schema_name.]trigger_name
ON {table|view}
{FOR|AFTER|INSTEAD OF}
{[INSERT][,][UPDATE][,][DELETE]}
AS
{sql_statement}
GO
```
- Enable/Disable/Drop Trigger

#ACID transact-sql
- atomicity
- consistency
- isolation
- durability

#Bulk Insert

#BigTable
- no table-wide integrity constraints
- no multi-row transactions
- no aggregation over data
- c++ functions, not sql
- clinet indicate what data to chache in memory

#db4o

#Three main aspects
- integrity
- availability
- confidentiality

#Four main control measures
- access control
- inference control
- flow control
- encryption

```
set nocount on
```


