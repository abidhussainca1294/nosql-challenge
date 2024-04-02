# nosql-challenge: Eat Safe, Love 
 
This project is performed for a food magazine, Eat Safe, Love to evaluate some of the ratings data in order to help their journalists and food critics decide where to focus future articles. The data from UK Food Standards Agency has been used for this purpose (UK Food Standards AgencyLinks to an external site. (2022). UK food hygiene rating data API. https://ratings.food.gov.uk/open-data/en-GB ).

The project comprises of two parts:

Part 1: Database and Jupyter Notebook Set Up and database update.
File: NoSQL_setup_starter.ipynb

1.  The data provided from UK Food standard Agency is imported from the terminal under the database name uk_food and the collection is named as establishments.
2. The database is reviewed using python libraries PyMongo and Pretty Print.
3.  A new restaurant named “Penang Flavours” is added to the database using PyMongo commands with the data in dictionary form.
4. Business Id as per the Business type in the data is updated to “Penang Flavors”
5. As the magazine is not interested in the establishments near Dover area, all the establishments near Dover area are found and removed from the collection. (994 establishments were removed.
6. Data type for longitude and latitude were changed to decimals and rating value into integer.

Part2: Exploratory Analysis
File: NoSQL_analysis_starter.ipynb

Specific questions from Eat Safe, love magazine was answered by performing analysis on the updated data. Pandas DataFrame were also created for final results and better understanding.

1. Which establishments have a hygiene score equal to 20?
Ans: 41 establishments have hygiene score of 20. A pandas DataFrame is created with these 41 establishments.

2. Which establishments in London have a `RatingValue` greater than or equal to 4?
Ans: A total of 33 establishments in London have rating value of 4 or more. Regex is used for matching London in authority name.

3.  What are the top 5 establishments with a `RatingValue` rating value of 5, sorted by lowest hygiene score, nearest to the new restaurant added, "Penang Flavours"?
Ans: Top 5 restaurants near Penang Flavours with maximum rating are extracted and arranged as per their hygiene score. The results are printed and displayed in pandas DataFrame too.

4. How many establishments in each Local Authority area have a hygiene score of 0?
Ans: For this a pipeline through the aggregate method has been used. The results were group by local Authority name and sorted in descending order of their counts. 55 Local Authority have establishments with zero hygiene. Panadas DataFrame is created with the authority’s name and total no. of establishment with zero hygiene.

