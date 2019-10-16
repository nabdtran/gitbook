# Business Logic Layer

### Microservices

Benefits of small separate services:

* Atomic, single-purpose code is easier to develop and maintain
* Does one thing and does it very well
* Supports A/B testing

Independently developed services aid in:

* Fault isolation
* Debugging
* Redundancy and resiliency

### App Engine

Microservices can be implemented on App Engine.

* Full code isolation
* Can be written in different languages
* Code executed through HTTP invocation/RESTful API

Limitations

* One master app per project

### GCP 12-Factor Support

One codebase tracked in version control with many deployments:

* Cloud Source Repositories or Github

Strictly separate build and run stages

* CloudBuild pipelines

Keep development, staging and production as similar as possible

* Deployment Manager Templates

Explicitly declare and isolate dependencies

* Custom images

Store config in the environment

* Metadata server, GCS

Maximize robustness with fast startup and graceful shutdown

* Instance templates, Managed instance groups and autoscaling.

### Kubernetes Engine

* Platform independence
* Separate application
* No OS dependencies
* Already using Kubernetes and need to scale
* Application can be containerised

### Horizontal Scaling

More server lifecycles to manage \(deployment complexity\)

* Automation makes this easy

End to end latency increases slightly

* Requirements will indicate whether the latency matters

More overhead, but unlikely to matter

* Outweighed by benefits in scaling and load balancing

#### Design

Keep servers simple: Do one thing well

* Minimize complexity
* Contruct simple and concise APIs

Prefer small stateless servers



