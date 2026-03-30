Okay. Now this is a little messy, but bear with me. 
Exam Guides - MongoDB Database Project
Author: Sebastian Eugene

Exam Guides is a study resource platform where students, professors, and researchers can create and access 
study materials organized by topic.


## Start here

Restore the database (instructions below)
1. Open STEP3 README to understand my collections structure
2. Then, open Step5(5 queries) to run the five required quries

## What the queries do -> (aggregation, search, count, update)

Query1: An aggregation on my Resource collection to calculate how many resources each account has.

Query2: Searches the Resource collection using a combination of operators to filter the documents based on conditions

Query3: Counts the number of documents in the Resource collection that are associated with a specific amount -> 
counts the amount of resources that belong to a specific account

Query4: Finds a specific user and switches their account activity between active and inactive

Query5: This gets all resources that are associated with a specific topic.

## Project structure

schema ->

Account.json Account collection code separated
Resource.json - Resource collection code separated
Topic.json - Topic collection code separated
Account_data.json - Account Mock data (Mockaroo generated)
Resource_data.json - Resource Mock data (Mockaroo generated)
Topic_data.json - Topic Mock data (Mockaroo generated)

docs ->
  Project Submission.pdf       - UML and Hierarchical ERD
  Database Project - App (2).pdf - problem requirements

dump ->
  examguides/       - MongoDB dump file for restoring the database

## Collections (3 main collections)

Account -> root collection. Stores Students, Professors, and Researchers using a role sorting field

Resource -> Stores Videos, Practice sets, and Text resources using a type field. Videos and Practice are embedded docs

Topic -> Independent reference collection. Resources point to Topics using topic_ID

## How to run the database

Using MongoDB, restore the database using

mongorestore --db examguides ./dump/examguides

Then run the queries in mongosh, pasting each query from step 5

## side notes for the ERD

Solid lines are embedded documents

Dashed lines are references

Purple lines are logical relationships






