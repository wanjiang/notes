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

```
case
  when then
end
```

```
open @m_cur

close @m_cur
deallocate @m_cur
```
