# Requirement
Calculate average cooking time per difficulty level for an ingredient

## Task 1
Using Apache Spark and Python, read, pre-process and persist rows to ensure optimal structure and performance for further processing.
The source events are located on the input folder.

## Task 2
Using Apache Spark and Python read processed dataset from Task 1 and:

Extract only recipes that have beef as one of the ingredients.
Calculate average cooking time duration per difficulty level.
Persist dataset as CSV to the output folder.
The dataset should have 2 columns: difficulty,avg_total_cooking_time.

Total cooking time duration can be calculated by formula:

total_cook_time = cookTime + prepTime


Criteria for levels based on total cook time duration:

easy - less than 30 mins
medium - between 30 and 60 mins
hard - more than 60 mins.

## Data Flow:

## Psuedo Code:
## Bonus Points:
### Config management
### Data quality checks
### implement CI/CD 
### Performance problems - Diagnose and tune
### Schedule pipeline periodically

