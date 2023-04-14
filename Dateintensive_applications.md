# Chapter 1: definitions

We want reliability,scalability and maintainablity of systems.

Scalability: When the `load` of your application increase, would it still `function as intended`.

`Load`: #resquests/sec, ratio of writes and reads from a DB

`Function as intended`: eg: Response time/latency. When measuring performance it makes sense to see latency at 99.9 quantile, eg: in case of amazon the users who
has longest response time == have more data for that customer/most important for amazon.

