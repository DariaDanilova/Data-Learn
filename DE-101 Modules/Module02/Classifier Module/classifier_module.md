### Goal
Implement a universal classifier module for classifying various entities.

### Description
Create two tables with the type of classifiers and their values, establish a relationship between them. Establish a relationship between the classifier and the tables for which classifications are applied.

### Initial data
There are tables *Client*, *Contract*, *Card* and similar ones for which you need to make a classification.

### Implementation
Since there can be many classifications, the option of creating multiple tables is not suitable. We need a universal way. You need to create two tables, as shown in the figure below.

![image](https://user-images.githubusercontent.com/61746700/175040120-c919c41e-4f8c-439b-b33d-73c63ed33ed4.png)

The *Classifer_type* table is responsible for the type of classifier – "*VIP status*", "*Security level*", "*Promo card*", etc. In this table, the *type_id* attribute is the classification id, *classifer_name* is the corresponding name ("*VIP status*", "*Security Level*", "*Promo card*"), *entity_name* is the name of the entity for which the classification is applicable, i.e. *Client*, *Contract*, *Card*, etc.

The *Classifier_values* table contains classification values (the *value* and *value_id* attribute) and *classifier_id*, which allows you to determine which type of classification the values belong to.

The *Classifier_type* table is the parent one, the *Classifier_values* table is the child one. The foreign key is the *classifier_id* attribute.

The *Classifer_type* table is linked to those tables (entities) for which classifications are created by a many-to-many relationship. The figure above shows the Client as an example.

Example, filling in the *Classifer_type* table:

![image](https://user-images.githubusercontent.com/61746700/175042006-f43c61a4-fa01-45fc-a0d3-11d93ecf0bba.png)

Example, filling in the *Classifier_values* table:

![image](https://user-images.githubusercontent.com/61746700/175042249-f6d76137-902f-47e6-9bb5-a27062ae629d.png)
