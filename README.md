# Architecture_of_a_Database_System

http://db.cs.berkeley.edu/papers/fntdb07-architecture.pdf

Roughly speaking, modern DBMSs implement isolation via a locking protocol. Durability is typically implemented via logging and
recovery. Isolation and Atomicity are guaranteed by a combination of locking (to prevent visibility of transient database states), and logging (to ensure correctness of data that is visible). Consistency is managed by runtime checks in the query executor: if a transaction’s actions will violate a SQL integrity constraint, the transaction is aborted and an error code returned.
