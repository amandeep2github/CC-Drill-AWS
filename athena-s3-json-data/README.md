# Use athena to query json data in s3

## Steps
- upload some json files without beautification to s3 bucket in folder say athena
- in aws console open athena, in workgroups for primary, choose edit and give output result location say at the  level parallel to folder athena say output
- in athena console again, datasources, create new data sources, choose s3 glue data catalog
- create table, give table name, choose database (can be existing), choose s3 location, choose dataset e.g. JSON, column details e.g. productname string, productId string, price float, timeofvisit timestamp
- create table and query

## Concepts
### aws
- athena saves result in a bucket location
- athena uses glue which is ETL tool to transform data in file formats to athena report
- athena uses hadoop to query data in s3
- everytime athena query is used, two files .metadata and .csv data files in created in output bucket