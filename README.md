# UK Food Standards Agency Data Analysis

This repository contains the code and analysis for evaluating the food hygiene ratings data from the UK Food Standards Agency. The analysis aims to assist the editors of a food magazine, Eat Safe, Love, in identifying establishments for future articles.

## Instructions

### Part 1: Database and Jupyter Notebook Set Up

1. Open the `NoSQL_setup_starter.ipynb` notebook.
2. Import the data provided in the `establishments.json` file into MongoDB. Use the following command in your Terminal to import the data:

```bash
mongoimport --db uk_food --collection establishments --drop --file establishments.json
```

3. Import the necessary libraries in the Jupyter Notebook, including PyMongo and Pretty Print (pprint).
4. Create an instance of the Mongo Client.
5. Confirm the successful creation of the database and loading of the data by performing the following checks:
   - List the databases in MongoDB and verify that `uk_food` is listed.
   - List the collections in the `uk_food` database and ensure that `establishments` is present.
   - Use the `find_one` method to display one document from the `establishments` collection and print it using `pprint`.
   - Assign the `establishments` collection to a variable for further use.

### Part 2: Update the Database

1. Continue working in the `NoSQL_setup_starter.ipynb` notebook.
2. Add a new document for an exciting halal restaurant called "Penang Flavours" located in Greenwich, which hasn't been rated yet. Use the provided information to create the document.
3. Find the `BusinessTypeID` for "Restaurant/Cafe/Canteen" and return only the `BusinessTypeID` and `BusinessType` fields.
4. Update the document of "Penang Flavours" with the correct `BusinessTypeID` you found.
5. Check the number of documents that contain the Dover Local Authority. Remove all establishments within the Dover Local Authority from the database and verify the deletion by checking the number of documents again.
6. Convert the following fields to their appropriate data types:
   - Convert the latitude and longitude fields from strings to decimal numbers using `update_many`.
   - Convert the `RatingValue` field to integer numbers using `update_many`.

### Part 3: Exploratory Analysis

1. Switch to the `NoSQL_analysis_starter.ipynb` notebook.
2. Answer the following questions by exploring the database and providing the required information:
   - Which establishments have a hygiene score equal to 20?
   - Which establishments in London have a `RatingValue` greater than or equal to 4?
   - What are the top 5 establishments with a `RatingValue` of 5, sorted by the lowest hygiene score, nearest to the new restaurant "Penang Flavours"?
   - How many establishments in each Local Authority area have a hygiene score of 0? Sort the results from highest to lowest and print the top ten Local Authority areas.

Each question should include the following steps:
- Perform a query to find the desired data.
- Use `count_documents` to display the number of documents in the result.
- Print the first document in the results using `pprint`.
- Convert the results to a Pandas DataFrame, print the number of rows, and display the first 10 rows.

## Deployment and Submission

The code and analysis files should be submitted in a GitHub repository cloned to your local machine. Use the command line to add your files to the repository and include appropriate commit messages.

## Comments

The code and notebook files should be well commented with concise, relevant notes explaining the purpose and functionality of the code. This will help other developers
