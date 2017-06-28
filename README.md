# Elastic Mockery

Used to mock the Elasticsearch python library. Creates portable fixtures that can be used to run Python unit tests offline. 

## Getting Started

Elastic Mockery is able to record the results of all the requests made to the elasticsearch-py library and store them in file.
This allows the user to run unit tests that expect data from Elasticsearch without actually needing an Elasticsearch server.

Elastic Mockery wraps the ElasticSearch client and whenever a request to one of the known search functions is made, it records all the parameters and creates a unique base64 key for these parameters. This key is used to name the file where the response will be stored for later offline requests.
