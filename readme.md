# NATS-DEMOS

A repository for tracking NATS patterns and Demo applications.

# Applications

Applications folder contains a set of demo applications that use various patterns for real world applications. Will contain the following:
* client
* server
* nats environment
* leveraged libraries
* Diagrams
* Architecture design record

# Environments
Environments is a programatic implmenetation of various different NATS environment configurations that can be called as part of demo applications and testing configurations.
The following environments have been implemented:
* single node: single nats server for simple test cases and validating basic functionality
* cluster: simple 3 node nats cluster, can be used for testing and validating cluster behavior or observing cluster behavior
* stretch cluster: single node per region cluster.
* supercluster(mesh): single node clusters connected via gateways in mesh
* supercluster(ring): three single node clusters connected in a ring topology via gateways
* supercluster(regional + stretch): three single node clusters connected in a mesh with corresponding regional connections to stretch cluster servers
* leafnode(leaf + cluster): leaf node server configured to talk to single node nats cluster

# Libraries
Libraries is a set of helper libraries for simplifying performing various tasks using NATS and NATS jetstream.
* locker: a locker helper library that creates a locker object. Supports lock update mechanism and timeout.
* typedKv: a golang generics typing abstraction over keyvalue store that takes a manages kvs as typed resources to validate writing and reading data back as specific type.
* fifoQueue: a first in first out queue implemented using nats key value store for tracking messages by subject and allowing multiple workers to process messages in the queue of different subjects
* watcherCache: a watcher service that implements an in memory key value store cache for watched key value store keys

# Patterns
Patterns is a set of implementation examples for common use cases found when interacting with nats and jetstream.
* workerQueue: 
* microservice:
* 