# Design

Correlaetd failures occur when related items fail at the same time.

A group of related items that could fail at one time is a failure domain.



Design to avoid correlated faulures

Decouple servers, use microservices

Failure due to overload

Overload failure is when a resource crosses into non-linear behaviour. It can crash, thrash disk, stop responding or break adjacent resources that the service depends on.



Fan-in \(incast\) overload failure.

Queries of death overload failure

Problem : Business logic error shows up as overconsumption of resources and service overloads.



Solution: monitor query performance iteratively. Ensure notification of these issues gets bac kto the developers.

Stackdriver trace



