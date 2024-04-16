# Data Engineering - ETL project using python and postgres

## Project overview
In this project the aim is to get the most important data about the used bmw3series listed on https://www.beforward.jp/ then transform the data into a data frame and load it into a data base which in our case was postgres.
#### important data includes
- vehicle reference number
- price
- total price(includes import charges)
- mileage
- color
- location
- engine capacity
- year

So, let`s get started.

Before we even get to our first stage we need to make sure we have imported all the Python packages we will need for this project.
![packages](https://github.com/EugeneMakanga/ETL_project/assets/166953108/57ac6424-590a-49b7-85b6-2f6dcbc431f2)


### Extract stage

For the key part of our project will first get the URL that leads to the listed type of cars specifically whose data we need to extract.
![scrapping](https://github.com/EugeneMakanga/ETL_project/assets/166953108/16bd138d-7958-4ca6-9b87-8b3534476e06)

Using that URL we will scrap the links to each individual vehicle after that we can extract the data we need.
![extracted data](https://github.com/EugeneMakanga/ETL_project/assets/166953108/a9433316-d3b6-41db-b96a-34a0d6fd2f27)


During this stage we use packages such as beautifulsoup and requests.

### Transform stage
After we have extracted the data needed, now it`s time to transform it into a data frame using the python package called pandas.
![data frame](https://github.com/EugeneMakanga/ETL_project/assets/166953108/65ad71d2-f12b-47ad-9cf9-1651afa8525a)

### Loading stage
In this stage we connect to postgres where we create our database.
![create database](https://github.com/EugeneMakanga/ETL_project/assets/166953108/b0e466ad-3f27-427e-bc8f-0436ccb8e734)

We use the python package called psycopg2,
with the database created let`s load our extracted and transformed data into it, here we use the create engine feature that is found in the sqlalchemy package.
![load](https://github.com/EugeneMakanga/ETL_project/assets/166953108/51eb52f0-c6db-496d-8b7e-64e30abbe8ee)
![loading](https://github.com/EugeneMakanga/ETL_project/assets/166953108/0cc9313d-3ec5-492d-ac53-14733397e624)

Here is how the final product looked like.

![loaded](https://github.com/EugeneMakanga/ETL_project/assets/166953108/614b54de-c9de-4193-9c9f-9d0645d704e4)


### References
resources used during the making of this project
- Her data project (Youtube channel on data analysis)
- Darshil Parmar (Youtube channel on data engineering)
