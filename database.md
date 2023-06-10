# DATABASE info I wish I know earlier

## Database management system

1. Normal forms, a good guidelines to designing schemas for relational database. 
Resource:
- https://www.geeksforgeeks.org/normal-forms-in-dbms/ 
  - consist of 1NF, 2NF ...

2. Keys

Note for PK (that you probably will miss)
- can only have one primary key (but can have composite primary key)
- updating constraint is crucial when changing primary key from one column to another
- normal forms are great for deciding which is the primary key 
- good to enforce the fact that primary key is unique (unique identifer) 
- no nulls are allowed in primary keys

Sth about foreign key
- foreign key constraints: tells the database that every column of the data in the foreign table must match the PK of the table it's linked to
-  a child table should contains the foreign key linking to the parent
-  can join foreign tables 

Composite key:
- key that contains more than one attribute
- simple key if only one 
- any foreign key that reference this composite key will also be composite (e.g. {coffe type, coffee size} -> pk : customer, fk: {coffee type, coffee size})
- nuances with compound key
  - compound key are sometimes referred to as a type of composite key that contains at least one attribute that's a foreign key to some other table

Candidate key:
- candidates for deciding which is the primary key (both unique)
- a key is irreducible if it only has the attributes it needs to have
- a candidate key should be irreducible

Super key 
- a key that contains all attributes it needs to have plus potentially some additional attributes 

Resource:
- https://www.youtube.com/watch?v=8wUUMOKAK-c&list=PLCLvWCKSCTAVkJjpf7fpYrwIFgjzYeMVL&index=9 

3. About joining

Resource: https://www.youtube.com/watch?v=G3lJAxg1cy8&t=2s
