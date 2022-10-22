# Database Architecture Lecture

## Structure: 

- Discuss important best practices

- Work on a e-commerce example together

- Today we won't be directly coding, but rather thinking in terms of structure/ diagrams

- If we have time, we will work in groups in a Twitter database example





















---------------





## Go back to how the web works

## Why do we need to think about archictecture

## Naming convention
 - postgress and other open source languages: snake_case
 - other communities (ex MSSQL - microsoft): PascalCase
 - tables names should be plural AND columns names singular


## Thinking which tables we need to create


## What data does those table need?


## Data Types

- look at docs
- most common: 
    * integer
    * varchar
    * text
    * boolean
    * date/time

## Key types (Primary Key x Foreign Key)

- Primary Key: 
    * need to be unique
    * can have any datatype but they are normally numbers (integers)
    * cannot be changed

- Foreign Key
    * used to relate 2 databases
    * need to have the same type as the one from the table you are relating it with


## Relationship between tables

- One to one
- One to many
- Many to many


## Design Concepts 

- Required Fields: make sure you know values that are mandatory to your database. This means security + consistency. Use NOT NULL
- Set a default value: to make sure you cannot get null values that may invalidate your logic
- Have a soft deletion approach: instead of 'dropping database' (which can cause tragic situations), you can add `isActive` field OR adding the entry to a 'deleted_info' database before moving forward
- Avoid calculated fields: leave it for the front and back end. Avoid possible inconsistencies on you DB
- Avoid arrays as types. If you think you should have an array just create a new table and skip some uncessary complexity

## ERDs - Entity Relationship Models

[DRAW.IO](draw.io)