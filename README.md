# Hello Fresh Data Engineer Assignement :

# Introduction

This project handles hello fresh requirement 

Requirement:
        Find average cooking time per difficulty level for an ingredient.

Detail explanation of job logic is explained in ETL_README.md

This project boiler plate is from : https://github.com/mehd-io/pyspark-boilerplate-mehdio

Requirements :
* Docker
* make
* Any Cloud Service that can run pyspark

## Development
### Build the dev image
```
make build-docker
```
### Run the tests
```
make test-docker
```
### Run the spark job demo_job
```
make run-docker
```
## Folder Structure

```
├── LICENCE
├── Makefile
├── README.md
├── sparkjobs
│   ├── configs // hold static config of the etl
│   ├── helpers 
│   └── jobs // main logic
├── docker // for dev container
├── poetry.lock
├── pyproject.toml
├── setup.cfg
├── setup.py
└── tests // test with fixtures data
└── input
└── output
└── error

```

## Configuration
Static configuration can be done through `./sparkjobs/configs/recipe_avgtime_config.py`

For instance : 
```
	spark-submit \
	--jars jars/spark-excel_2.11-0.9.9.jar \
	--py-files sparkjobs.zip \
	sparkjobs/jobs/recipe_avgtime_job.py

```
will run the job `sparkjobs/jobs/recipe_avgtime_job.py` and the associated config value from `./sparkjobs/configs/recipe_avgtime_config.py`.

## Package
You need the following files/zip : 
* python dependencies that include your spark code(as .zip)

To run a ready depencies folder as `.zip` run : 
```
make package
```
will generate a `sparkjobs.zip`

## Launching your spark job

```
	spark-submit \
	--py-files sparkjobs.zip \
	datajob/cli.py \
	sparkjobs/jobs/recipe_avgtime_job.py
```

`--py-files`: python libs, python source code

`sparkjobs/jobs/recipe_avgtime_job.py`: ETL job 


# References:
https://github.com/mehd-io/pyspark-boilerplate-mehdio
https://github.com/AlexIoannides/pyspark-example-project
https://developerzen.com/best-practices-writing-production-grade-pyspark-jobs-cb688ac4d20f
https://realpython.com/pipenv-guide/
