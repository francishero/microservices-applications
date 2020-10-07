## Microservices 101
Microservices, Event Driven, Pub-Sub, Docker, Kubernetes, CI/CD etc.

## Author
Aditya Hajare ([Linkedin](https://in.linkedin.com/in/aditya-hajare)).

## Current Status
WIP (Work In Progress)!

## License
Open-sourced software licensed under the [MIT license](http://opensource.org/licenses/MIT).

----------------------------------------

## Notes

```diff
+ Why Database Per-Service
```
- We want each service to run independently of other services.
- Database schema/structure might change unexpectedly.
- Some services might function efficiently with different types of DB's (SQL vs. NoSQL).

----------------------------------------

```diff
+ Communication Strategies Between Services
```
- **Sync**: Services communicate with each other using direct requests.
    * Conceptually easy to understand.
    * Service won't need a database.
    * Introduces a dependency between services.
    * If any inter-service request failes, the entire service fails.
    * The entire request is only as fast as the slowest request.
    * Can easily introduce webs of requests.
- **Async**: Service communicate with each other using **events**.

----------------------------------------
