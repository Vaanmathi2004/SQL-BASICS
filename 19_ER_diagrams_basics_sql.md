# ER DIAGRAMS
- ER refers to `Entity relationship`
- When you're designing a database, one of the important thing is designing a database schema.
- We can use ER diagram to act as a middleman between the database or storage requirements and the actual database schema.
- ER diagram is a great way to take the data storage requirements like business requirements and convert them into an actual database schema.
- We can use ER diagram to map out the different relationships and the different entities and the different attributes for those entities.
- It can be really a great way to organize our data into a databse schema.
- ER diagram is a little diagram that consists of different shapes and symbols and texts and all gets combined together to end up defining a relationship model. 
-----
- Let's take a example of designing a database schema or to design an ER diagram for our database for the school.

## Different parts of ER diagram

### ENTITY
- An object we want to model and store information about.

Ex:

`student`

- Entity is gonna be square like this, and we are having the name of the entity that we're storing.

### ATTRIBUTES
- Specific piece of information about an entity.

        Student
       /  |     
      /   |      
    name       gpa

- name and gpa are attributes that are ovals and are connected to entity.

### PRIMARY KEY

- An attribute that uniquely identify an entry in the database table.
- Whenever we're defining a primary key, we're going to underline.

### Composite attribute
- An attribute that can be broken up into sub-attributes.

      Student

       /  |     
      /   |      
    name       gpa

    /    |
   
fname   lname

### Multi- valued attribute

- If there's any attribute in your data model that could have more than one value
- Doubly ovaled 

Ex: Clubs
- Student might be involved in various clubs.
- So, clubs is a mutli-valued attribute (it could have more than one value).

### DERIVED ATTRIBUTE

- Attribute that can be derived from the other attributes that we're keeing track of.
- We're not going to keep track of the derived attribute, it's just a way that we can sort of notate attributes that could be derived from the attributes that we're storing.
- Oval with the dotted lines. 

Ex: has_honor

- This is an attribute that we can derive from the gpa.


### MULTIPLE ENTITIES

- We can define more than one entity in the diagram.

Ex: student, class
___

### Relationship

- When we have two entity, we want to define relationships between those entities.
- Relationship is the shape of diamond connecting both the entities.

`takes`   - verbal

  Ex: students is going to take class, class can be taken by the student. (student and class are related in both the ways)

- We connect the entity with the relationship(diamond) using line.

Ex: 
- Student is connected with the relationship using `single line`. (Partial participation) - Not necessarily all the students have to take a class.

`Partial participation - Not all the members have to participate in the relationship`
- Class is connected with the relationship using `double line`. (Total participation - All the classes have to be taken by atleast a single student)

`Total participation - All the members must participate in the relationship`

### Relationship attribute

- An attribute about the relationship

takes

|

grade

- Student will take a class and the student will get a particular grade for that class.
- This grade attribute need not to be necessarily stored on the student entity nor on the class entity. It's stored on the relationship

### Relationship cardinality

- The number of instances of an entity from a relation that can be associated with the relation

Ex: A student can take any number of classes

`N M`

N- Class taken by any numbe of students

M- Number of classes taken by the student.

- This can be like 

`1:1` - A student can take one class and a class can be taken by one student

`1:N` - A student can take one class and a class can be taken by many students

`M:N` - A student can take any number of classes and a class can be taken by many students

- It's useful to define that relationship cardinality in ER diagram because that's actually going to relate to how we want to design our database schema
- RC could be defined in data modeling requirements. 
- If the requirements comes to you and says a student can only take one class at a time, that you want to be able to represent inside of the ER diagram.

### WEAK ENTITY 

- An entity that cannot be uniquely identified by it's attributes alone.
- Entity that depend on another entity.

Ex:

- Class entity relates(has) to exam entity.
- But an exam can't exist without a class.
- An exam have to exist, it has to be associated with a class.

### IDENTIFYING RELATIONSHIP

- A relationship that serves to uniquely identify the weak entity.

Ex: 
- An exam entity can be uniquely identified if it is paired with class entity. (Class had a exam and an exam is had by a class) `Has`

- The weak entity have to have a total participation with the
identifying relationship.
(All exams must have class but not all classes have to have exam)

- Weak entity is represented by double square and it's primary attribute is represented by dotted underlines.


