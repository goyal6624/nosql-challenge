# nosql-challenge

This module challenged my ability to use a NoSQL database with MongoDB controlled by `PyMongo`. The Jupyter Notebook `NoSQL_setup.ipynb` sets up the database, making sure it is fully clean and formatted properly with the correct data types for each entry parameter. Then, `NoSQL_analysis.ipynb` retrieves all of the information needed to conduct an analysis from the database to answer a select number of questions, and converts the resultant answers to a `pandas` DataFrame.

## Methodology

To set up the database, I did the following:

- Changed my directory (`cd`) into `Resources`
- Ran `mongoimport --db uk_food --collection establishments --file .\establishments.json --jsonArray` from the terminal
- Imported all dependencies for both notebooks
- Created an instance of MongoClient on port 27017 to access the `uk_food` database.

## Exploratory Analysis

1. Which establishments have a hygiene score equal to 20?

- There are 41 total establishments with a hygiene score = 20. To see the full list of them, see `NoSQL_analysis.ipynb`

2. Which establishments in London have a `RatingValue` $\ge$ 4?

- There are 33 total establishments in London with a `RatingValue` $\ge$ 4. To see the full list of them, see `NoSQL_analysis.ipynb`

3. What are the top 5 establishments with a `RatingValue`` rating value of 5, sorted by lowest hygiene score, nearest to the new restaurant added, "Penang Flavours"?

- ['Volunteer', 'Plumstead Manor Nursery', 'Iceland', 'TIWA N TIWA African Restaurant Ltd', 'Howe and Co Fish and Chips - Van 17']

4. How many establishments in each Local Authority area have a hygiene score of 0?

- There are 55 cities containing establishments with a hygiene score of 0. For a list of the first ten cities in ascending order, see `NoSQL_analysis.ipynb`
