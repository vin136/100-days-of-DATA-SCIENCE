# Chapter 1: definitions

We want reliability,scalability and maintainablity of systems.

- reliability: function as intended despite hardware faults, software failures.

- Scalability: When the `load` of your application increase, would it still `function as intended`.

`Load`: #resquests/sec, ratio of writes and reads from a DB

Approaches for coping with load : vertical scaling or horizontal scaling (usally hybrid)

`Function as intended`: eg: Response time/latency. When measuring performance it makes sense to see latency at 99.9 quantile, eg: in case of amazon the users who
has longest response time == have more data for that customer/most important for amazon.

- Maintainability = #good abstractions + extendability of code + telemetry/observability.

-----------------

# Data Models and Query languages

- Level 1: At application level we model the world with objects and relationships between them.

- Level 2: We got to be able to store and retrieve this data for future. We hand it over to DB's which store and represent it some ways.(store: Relational tables, Document based(mongodb), graph based(neo4j), retrieve: imperative vs declarative.

- Level 3: How the DB stores and retrieves data. (stores:write only log-files,B-trees, retrieves:indexes)


`Relational DB's/SQL`: Breaks the data into multiple tables. Imagine storing a resume which is naturally represented by JSON but if we'r going for RDBMS, we got to split it into distinct tables like position,education etc and use foreign key to connect them.

`NoSql(not only sql)`: Most popular is document model. Store data inthe form of documents/json. This makes sense when your application has document-level/local access patterns.

`Case for Graph Storage`: Imagine storing the data of people and their relaionships as they evolve. No definite nodes, and lot's of many-many relationships.

When there are lot's of many-many relationships,lot of variablity in data = Graph representation becomes more natural.

--------------------

Data storage and retrieval

OLTP : row-based. read: at most mg,write:random access.

OLAP: column store (find all the order's from a store).

For data-warehouse star-schema: fact and dimensions table.

