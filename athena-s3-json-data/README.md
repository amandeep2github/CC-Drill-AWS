# Use athena to query json data in s3

## Steps
- upload some json files without beautification to s3 in folder say athena
- in aws console open athena, in workgroups for primary, choose edit and give output result location say at the same level in athena, output
- in athena console again, datasources, create new data sources, choose s3 glue data catalog
- create table, give table name, choose database (can be existing), choose s3 location, choose dataset e.g. JSON, column details e.g. productname string, productId string
- create table and query

## Concepts
### aws
- athena saves result in a bucket location
- athena uses glue which is ETL tool to transform data in file formats to athena report