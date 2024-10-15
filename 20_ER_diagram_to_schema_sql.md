# CONVERTING ER DIAGRAM INTO SCHEMAS

- From the data requirements, we're designing the ER diagram.
- Then we convert this ER diagram into database schema.

## STEPS TO CONVERT:

1. **Mapping of regular entity types**
     - For each regular entity type create a relation (table) that includes all the simple attributes of the entity.
     (Entity- Table name, Attributes - column)
     - Composite attribute are stored as sub attributes 
     `name - composite attribute
     F_name, L_name - sub attributes
     `  
     - The columns will be F_name, L_name.
2. **Mapping of weak entity types**
    - For each weak entity type, create a relation (table) that includes all simple attributes of the weak entity
    - The primary key of the new relation should be the partial key of the weak entity and the primary key of it's owner. (composite key)

3. **Mapping of Binary 1:1 relationship types**
    - Binary (two entities particpating)
    - Include one side of the relationship's primary key as a foreign key in the other favor total participation.
    - If there is total participation from both sides, we can decide ourselves.


4. **Mapping of Binary 1:N relationship types**
    - Include the 1 side's primary key as a foreign key on the N side relation (table)

5. **Mapping of Binary M:N relationship types** 
    - Create a new relation (table) who's primary key is a combination of both entities's primary key's. Also include any relationship attributes.
    (We gonna create new table for this)

---
**Pointing:**
- foreign key points to it's main attribute (arrow mark)
- Primary key being foreign key also points to it's main relation. 
