# Book Indexer (NodeJS)

Training project demonstrating AWS SQS receive messages and ElasticSearch Indexing. This project implements a nodejs application that should be listening on a queue in AWS. When a new message appears in the queue the appplication takes this message and indexes it in ElasticSearch. Each message is generated from an operation that can be Insert, Update or Delete. According to the type of operation the application indexes or removes an indexed value in ElasticSearch.


## Run

`$ npm start`
