# About 
This assignment was submitted on 12th Oct 2019 as part of the Knowledge Graphs class in MITB. 

## Task 
The requirements were to:
1. Scrape infoboxes of cities in a given `cities.xml` list from Wikipedia. (Without using DBPedia)
2. Clean the scraped data (Remove unmeaningful characters and combine bullet points with their preceding headers)
3. Generate triples for all of the infoboxes
4. Write the triples to a `.nt` file
5. Upload the `.nt` file to Apache Jena and query the cities whose country is Afghanistan.

## Overview
Steps taken were roughly as outlined in the [ipynb](./Submissions/Assignment1_GeraldinePang.ipynb):
1. Extract 
    - Created a `Handler()` class to practice some OOP concepts. 
    - Scrape data from Wikipedia using `BeautifulSoup4`. `Threading` was used to speed up the process. 
    - Parse for Bullet points 
    - Handle missing infoboxes (e.g. pages that point to disambiguation pages) by performing altered/additional searches
2. Transform
    - Clean the data according to the requirements, handle some illegal characters in the strings
    - Convert into triples using the `rdflib` package.
    - Serialize into an `.nt` file and save it for submission
3. Load
    - Run Apache Jena using the Docker mirror as described [here](https://hub.docker.com/r/stain/jena-fuseki/)
    - Using **SPAQRL**, run the required query to obtain the correct result.

# To Use
Refer to the [ipynb](./Submissions/Assignment1_GeraldinePang.ipynb) under the [Submissions](./Submissions) directory. 

## Requirements 
Python3.7. Packages are listed in the requirements.txt.

## Credits
Much thanks to [Shide Foo](github.com/shydefoo) for recommendations for improving the scraping. 