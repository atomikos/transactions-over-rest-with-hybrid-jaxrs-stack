# transactions-over-rest-with-hybrid-jaxrs-stack

Sample to demonstrate how to propagate transactional context accross 2 web services through rest, each service using a different JAXRS implementation. 

## One "account server" with Jersey + Spring DATA (Hibernate)

This service manages accounts and is called by the client inside a transaction.

## One "client" with CXF client + Spring DATA

The client creates a payment in its local database and creates an account through a transactional REST call.

Thanks to a "Command line Runner" the demo makes a call that works (commit) and another one that fail (rollback).
