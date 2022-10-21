## Go back to how the web works

- The importance of data
- Databases are composed by tables
- What are tables composed of? Rows and Columns
- Typically tables are named using snake_case
- Tables are named in plural as a best practice, example: users, pets, etc

(create a model for cats and dogs breeds)

## Recap on keys:
- Primary Key: 
    * Unique in the database
    * It can be any data type but most commonly they are integers
    * Every table needs a primary key
    * It is a value that you don't ever want to change

- Foreign Key
    * It is used to relate two tables together
    * They should be the same data-type as the primary key of the table you want it to be related to


## Naming convention

- Postgress and other open source databases use adopt snake_case as best practice
- Other databases may adopt different conventions. For example MSSQL (from Microsoft) uses PascalCase
- Best practices means that it is a recommended practice within the community but not enforced by the language
- Other best practice: table's name should be plural. And the column singular

## Datatypes in SQL
[DOCS](https://www.postgresql.org/docs/current/datatype.html)

- Prefer the types that are shared between databases. 
- Nothing wrong with keeping up with 'simpler' types:
        * Integer
        * Character
        * Date/Time
        * Boolean

## Possible Relationship Types
- One-to-one
- One-to-many
- Many-to-many

## Design Concepts 

- Required Fields: make sure you know values that are mandatory to your database. This means security + consistency. Use NOT NULL
- Set a default value: to make sure you cannot get null values that may invalidate your logic
- Have a soft deletion approach: instead of 'dropping database' (which can cause tragic situations), you can add `isActive` field OR adding the entry to a 'deleted_info' database before moving forward
- Avoid calculated fields: leave it for the front and back end. Avoid possible inconsistencies on you DB
- Avoid arrays as types. If you think you should have an array just create a new table and skip some uncessary complexity

## ERDs - Entity Relationship Models

[DRAW.IO](draw.io)