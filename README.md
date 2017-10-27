# Book Indexer (NodeJS)

Training project demonstrating AWS SQS receive messages and ElasticSearch Indexing. This project implements a nodejs application that should be listening on a queue in AWS. When a new message appears in the queue the appplication takes this message and indexes it in ElasticSearch. Each message is generated from an operation that can be Insert, Update or Delete. According to the type of operation the application indexes or removes an indexed value in ElasticSearch.

**Example of queue message:**
```json
 {
   "object": {
     "id":"59f32438f36dd63724b52904",
     "title": "Genghis Khan and the Making of the Modern World",
     "author": "Jack Weatherford",
     "genre": "History"
   }, 
   "operation": "Insert", 
   "queue": "https://sqs.us-east-2.amazonaws.com/404669482207/book-track.fifo"
 }
```

## Set up

### AWS Credentials
The application uses your **default** credential profile by reading from the credentials file located at (~/.aws/credentials).
For more information about see [Configuration and Credential Files](http://docs.aws.amazon.com/cli/latest/userguide/cli-config-files.html)

## Run

`$ npm start`
