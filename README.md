# Wikipedia-API

# Overview

This program is built to connect to the Wikipedia API and pull the names of famous individuals born between 1865 and 2015 along with their occupation.

# Process 

To begin this program we connect to our Wikipedia API and set our requirements for the query. 

To pull the desired results for each year between 1865-2015 we will need to initialize a for loop to iterate over each year as well as set up pagination to pull multiple pages per each year.

We handle both of these issues in the final build section. First we initialize an empty set called last continue, this will serve as a counter of sorts that tells our function to either continue to the next page for a set year or move to the next year. We also define pages and year list.

Then we initialize our for loop that requests a query from the API for every year within our YEARS list. We also update the last continue set and initialize our iteration counter.

Within the for loop is a while loop, here we begin by returning the results from our API query. From these results we assign the names of the individuals pulled for that year to our people dictionary. Then we print the number of pages we have pulled and the length of the People dictionary's items pulled in that iteration.

Finally we come to our if statements, if continue is not in the result we break free of the while loop and repeat the process for the next year, if continue is in the results we replay the while loop for the same year querying the next page of results for that year.

Finally I write out the results to a text file with defined headers stating the year, name, and occupation for each entry from the People dictionary.
