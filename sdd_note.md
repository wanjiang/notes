#PROJECT #5
##[Dynamic loading](http://tldp.org/HOWTO/Program-Library-HOWTO/dl-libraries.html)
  - In Linux, DL libraries aren't actually special from the point-of-view of their format; they are built as standard object files or standard shared libraries as discussed above. The main difference is that the libraries aren't automatically loaded at program link time or start-up; instead, there is an API for opening a library, looking up symbols, handling errors, and closing the library. C users will need to include the header file <dlfcn.h> to use this API.
  - is a mechanism by which a computer program can, at run time,load a library into memory,retrieve the addresses of functions and variables contained in the library, execute those functions or access those variables, and unload the library from memory. 
  - Unlike static linking and dynamic linking, dynamic loading allows a computer program to start up in the absence of these libraries, to discover available libraries, and to potentially gain additional functionality.
  - Dynamic loading is most frequently used in implementing software plugins. For example, the Apache Web Server's *.dso "dynamic shared object" plugin files are libraries which are loaded at runtime with dynamic loading. Dynamic loading is also used in implementing computer programs where multiple different libraries may supply the requisite functionality and where the user has the option to select which library or libraries to provide.


##Static linking

##Dynamic linking

#PROJECT #4

##Numpy
NumPy is the fundamental package for scientific computing with Python. It contains among other things:
- a powerful N-dimensional array object
- sophisticated (broadcasting) functions
- tools for integrating C/C++ and Fortran code
- useful linear algebra, Fourier transform, and random number capabilities

##matplotlib

#PROJECT #3
Logic AI automatic reasoning

### Truth table

|p | q | p&amp;q | p&#124;q | p-&gt;q | not(p)&#124;q| 
|:--|---|-----|-------|------|-----------|
|0 | 0 |  0  |  0  |  1   |    1| 
|0 | 1 |  0  |  1  |  1   |    1| 
|1 | 0 |  0  |  1  |  0   |    0| 
|1 | 1 |  1  |  1  |  1   |    1| 


#### modus ponens
```
not(p) | q \
             -> q
    p      /
```
```
       | q \
             -> q
           /
```
#Dynamic programming Distance of two string
global sequence alignment using Needleman/Wunsch

match    +2
mismatch -1
gap      -2


#PROJECT #6
training case - first two files

|doc     |        |          | class|
|:-------|--------|----------|------|
|Chinese | Beijing|  Chinese |   c  |
|Chinese | Chinese|  Shanghai|   c  |
|Chinese | Macao  |          |   c  |
|- - - - |- - - - |- - - - - |- - - |
|Tokyo   | Japan   | Chinese   | j    |

```
Chinese  Chinese  Chinese Tokyo Japan ?
```

#### P(c) = 3/4, P(j) = 1/4
We use this: Prob1 = (nwordsByA1/nwordsByAs)

P(word|class) = [COUNT(word in class) + 1]/[The total words in the class + |v|]

:|v| the number of unique words in all class

- P(Chinese|c) = (5+1)/(8+6) = 3/7
- ...
- P(Tokyo|c) = (0+1)/(8+6) = 1/14
- P(Japan|c) = (0+1)/(8+6) = 1/14
- P(Chinese|j) = (1+1)/(3+6) = 2/9
- P(Tokyo|j) = (1+1)/(3+6) = 2/9
- P(Japan|j) = (1+1)/(3+6) = 2/9

```
Answer:
1. P(c|testdoc) 
P = P(c) x P(Chinese|c) x P(Chinese|c) x P(Chinese|c) x P(Tokyo|c) x P(Japan|c)
  = 3/4  x 3/7          x 3/7          x 3/7          x 1/14       x 1/14
  = 0.0003
2. P(j|testdoc) 
P = P(j) x P(Chinese|j) x P(Chinese|j) x P(Chinese|j) x P(Tokyo|j) x P(Japan|j)
  = 1/4  x 2/9          x 2/9          x 2/9          x 2/9        x 2/9 
  = 0.0001
Since 0.0003>0.0001
Chinese  Chinese  Chinese Tokyo Japan is c 
```

#VI
- :set ic  ignore case
- :set nonu
- :set number
- %
- syntax on
-        off
- insert
- moving around
- :
- /find
- f blank
- ; repeat
- Ctrl Down
- Ctrl Up
- H
- L
- M
- :23
- Ctrl g
- mb   mark
- 'b   back to mark
- dtf  delete to the "f"
- :|, $ s/...
- :|, %
- :n   :#
- :e   fn
- :split
- :vsplit
- yy   to buffer

#ER
### High-level Conceptual Data Models for DB Design
Steps:
  - Conceptual DB design
  - Logical DB design
  - Physical DB design

### ER Schema Diagram

### ER Model Concepts
- Entities, Attributes, and Values of Attributes

### Type of Attributes
- simple vs. composite (first name vs full name)
- single-valued vs. multi-values (car age vs. car colors)
- derivable (age from birth date)
- null

### Entity Types, Value Sets, and Key Attributes
- Entity Types defines schema for an entity set
- Value Sets are domains of values
- Key Attributes unique identifying attribute for each entity

### Relationships, Roles, and Structual Constraints
- A realationship is a subset of Cartesian Product of E1xE2...xEn of the 
  entities participating in the relation
- Degree of the relationship is the number of entity types
- Binary relationships and Ternary relationships
- Sometimes relationship may be viewed as attribute
- Role names and Recursive Relationships
- Constraints on Relationship Types
  - Cardinality ratio: 1:1, 1:N M:N
  - Participation constraint
- Attributes of Relations
  - 1:1 can migrate to either entity
  - 1:N can migrate to the N side
- Weak Entity Types: have no key attribute of their own

### Notation for ER Diagrams (min,max)
- (1,1): an employee must participate in exactly 1 works_for relationship with 
  a department
- (0,1)
- (4,N)

### Proper Naming of Schema Constructs
- Singular names for entities
- Nouns -> entities
- Verbs -> relationships

### Relational Model Concepts
- Domains: ints, floats..
- Attributes
- Tuples
- Relations (tables)
- Predicate (Prolog)

### Relational Model Constraints
- Domain constraint
- Key constraint
- Entity Integrity constraint
- Referential Integrity constraint
- Semantic Integrity constraint

### Relational Database Design Using ER-to-Relational Mapping Steps
- 1.Create a relation for each regular entity type.Choose primary keys.
- 2.Create a relation for each weak entity type.Include a foreign key back to 
  the owner entity type's primary key
- Handle 1:1 relationship type
- Handle 1:N relationship type
- Handle M:N relationship type
- Handle multi-valued attrubutes
- Handle N-ary relationship types

#Design Pattern 
[GOF Gof4 Nutshell book ASPN](http://legacy.python.org/workshops/1997-10/proceedings/savikko.html#gof)
##Types of patterns:
```
Patterns are not invented, they are discovered.
```
- Creational patterns
  - patterns provide a way to create objects while hiding the creation logic, rather than instantiating objects directly using a new operator.
```
address object instantiation issues
```
- Structural patterns
```
concentrate on object composition and their relations in the runtime object structures, describe the layout of the object system.
```
- Behavioral patterns
```
focus on the internal dynamics and object interaction in the system
```
##Principles
- Program to an interface not an implementation
- Favor object composition over inheritance

##Patterns
- Singleton (creational)
  - limit the number of the instances of the class to one
  has only one singleton
  create singleton of any class
- Borg
  - multiple instances but share the same state
- Itgen
- Observer
- Adapter
- Chain of Responsibility (behavioral)
  - create a system that can serve different requests in a hierarchical manner.
  In other words if an object that is a part of the system does not know how
  to respond to the given request it passes it along the object tree.
  It is often used in the context of graphical user interfaces where one
  widget may contain several other widges.
- Absfact
  python 
    - `__init__` constructor 
    - `__new__` will become the main constructor can create instance of any class
              like Factory
- Proxy (strutural)
  - an object has to be shielded from its clients.There may be a number of reasons for this: reference counting, different levels of access rights, lazy evaluation of the state of the object and so on.
- Iterator (behavioral)
- Command (behavioral)
- Dependency Injection (creational)
- Facade (structural)
  used for interface simplification
- Adapter (structural)
  all about altering the interface
- Decorator

#Prolog

#Unix
The shell is actually a full programming language, with variables and functions, and also arrays, being directly linked to the kernel, it has native file I/O primitives built into its very synatax, as well as process and job control.

- Everything is a file
- Pipeline
    - pipes introduced the idea of having stdin and stdout, through which the data would flow.
    - One process creates output, which becomes input to another command.
    - The Unix pipes method introduced a concept that dramatically affected the design of the rest of the system.
    - Most commands have a file argument as well, but existing commands were modified to default to read from their stdin and stdout
    - The pipe can then "stream" the data from one tool to another.
    - It makes the whole system a set of generiacally useful tools, as opposed to monolithic, single-purpose applications.
    - This has been summarized as "do one thing and do it well"
    - The GNU project still sticking to the "do one thing and do it well"
    - who | wc -l

#GNU (GNU's Not Unix)

#Linux
