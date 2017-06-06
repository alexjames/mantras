# Too Big NOT to Fail - Pat Helland, Simon Weaver, and Ed Harris

At webscale, homogenous infrastructure are easier to manage then heterogeneous ones. Larger number of 
commodity servers are prefereable than a few powerful ones. A 100 duck sized horses are better than 
one horse-sized duck because it becomes a single point of failure.

By the law of big numbers. individual pieces may be unreliable but the aggregate failure rate is predictable.
This means that you can't predict if a particular server will fail, but you can accurately predict that X
servers will fail by the end of the year. Predictablity matters more than reliability.

Commercially available data center hardware becomes cheaper, more powerful and consume lesser power as time 
goes on This is why it doesn't make sense to have hardware sitting around doing nothing. Also, most data
center hardware is never kept around for more than 3 years.

Simple model for server and service behaviour:
 * Any component can fail and the system must continue without human intervention.
 * The underlying system provides support for deployment and rollback.
 * If it can't be controlled with software, don't let it happen.

Integrated development, test, and deployment are built deeply into the system with controlled and automated deployment of software.
