#PROJECT #3
Logic AI automatic reasoning

### Truth table

|p | q | p&amp;q | p&#124;q | p-&gt;q | not(p)&#124;q| 
|:--|---|-----|-------|------|-----------|
|0 | 0 |  0  |  0  |  1   |    1| 
|0 | 1 |  0  |  1  |  1   |    1| 
|1 | 0 |  0  |  1  |  0   |    0| 
|1 | 1 |  1  |  1  |  1   |    1| 


modus ponens
not(p) | q \
             -> q
    p      /

       | q \
             -> q
           /

+------------------------------------------------------------------------------+
Dynamic programming Distance of two string

match    +2
mismatch -1
gap      -2

+------------------------------------------------------------------------------+

*PROJECT #6
training case - first two files

doc                        class
--------------------------------
Chinese  Beijing  Chinese    c
Chinese  Chinese  Shanghai   c
Chinese  Macao               c
- - - - - - - - - - - - - - - -
Tokyo    Japan    Chinese    j
--------------------------------
Chinese  Chinese  Chinese Tokyo Japan ?

P(c) = 3/4, P(j) = 1/4
We use this: Prob1 = (nwordsByA1/nwordsByAs)

P(word|class) = [COUNT(word in class) + 1]/[The total words in the class + |v|]

:|v| the number of unique words in all class

P(Chinese|c) = (5+1)/(8+6) = 3/7
...
P(Tokyo|c) = (0+1)/(8+6) = 1/14
P(Japan|c) = (0+1)/(8+6) = 1/14
P(Chinese|j) = (1+1)/(3+6) = 2/9
P(Tokyo|j) = (1+1)/(3+6) = 2/9
P(Japan|j) = (1+1)/(3+6) = 2/9

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

+------------------------------------------------------------------------------+

*VI
:set ic  ignore case
:set nonu
:set number
%
syntax on
       off
insert
moving around
:
/find
f blank
; repeat
Ctrl Down
Ctrl Up
H
L
M
:23
Ctrl g
mb   mark
'b   back to mark
dtf  delete to the "f"
:|, $ s/...
:|, %
:n   :#
:e   fn
:split
:vsplit
yy   to buffer

+------------------------------------------------------------------------------+

*ER
- High-level Conceptual Data Models for DB Design
  * Steps:
  - Conceptual DB design
  - Logical DB design
  - Physical DB design

ER Schema Diagram

ER Model Concepts
- Entities, Attributes, and Values of Attributes

Type of Attributes
- simple vs. composite (first name vs full name)
- single-valued vs. multi-values (car age vs. car colors)
- derivable (age from birth date)
- null

Entity Types, Value Sets, and Key Attributes
- Entity Types defines schema for an entity set
- Value Sets are domains of values
- Key Attributes unique identifying attribute for each entity

Relationships, Roles, and Structual Constraints
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

Notation for ER Diagrams (min,max)
- (1,1): an employee must participate in exactly 1 works_for relationship with 
  a department
- (0,1)
- (4,N)

Proper Naming of Schema Constructs
- Singular names for entities
- Nouns -> entities
- Verbs -> relationships

Relational Model Concepts
- Domains: ints, floats..
- Attributes
- Tuples
- Relations (tables)
- Predicate (Prolog)

Relational Model Constraints
- Domain constraint
- Key constraint
- Entity Integrity constraint
- Referential Integrity constraint
- Semantic Integrity constraint

Relational Database Design Using ER-to-Relational Mapping Steps
- 1.Create a relation for each regular entity type.Choose primary keys.
- 2.Create a relation for each weak entity type.Include a foreign key back to 
  the owner entity type's primary key
- Handle 1:1 relationship type
- Handle 1:N relationship type
- Handle M:N relationship type
- Handle multi-valued attrubutes
- Handle N-ary relationship types

+------------------------------------------------------------------------------+

Design Pattern GOF Gof4 Nutshell book ASPN
- Singleton
  has only one singleton
  create singleton of any class
- Borg
  multiple instances but share the same state
- Itgen
- Observer
- Adapter
- Chain
- Absfact
  python 
    - __init__ constructor 
    - __new__ will become the main constructor can create instance of any class
              like Factory

+------------------------------------------------------------------------------+

Prolog

+------------------------------------------------------------------------------+
