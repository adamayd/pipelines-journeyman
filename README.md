# Welcome to Pipelines
## A Journey in to Software Delivery, Automation and Infrastructure(Topics in DevOps and SRE'ing)

![Image of Pipelines](https://ausenco-www-staging.s3.amazonaws.com/upload/user/image/image_of_ambatovy-slurry-pipeline20180419180101551.jpg)

# Lets Set the Scene

You just started at a new role at pretty cool startup. They're making some big waves, and growing, but they're initial Architecture and Infrastructure isn't really prepared for the future. The initially set everything up by hand on an on prem server. There is absolutely no automation here. You've walked into poor documentation, and fully manual changes. Time for a digital transformation.

# The Job

Our Job is going to be be take this startup from Zero to Hero. We'll be required to do the following:

1. Distribute the System
2. Implement Source/Version Control, and a development strategy
3. Setup a CI/CD...CD(Possibly) pipeline for our code to move from Developers computers all the way to Production
4. Convert "MonoRepo" to Microservice Architechture
5. Ensure All(Or all that can be) Infrastructure is codified
6. Provide Visibility into the health of the Infrastructure and Applications
7. This app is a money maker. Let's make sure it can handle errors


## Distributed Systems

2020-05-16

### What are Distributed Systems??

A distributed system in its most simplest definition is a group of computers working together as to appear as a single computer to the end-user.

These machines have a shared state, operate concurrently and can fail independently without affecting the whole system’s uptime.

### Why are Distributed Systems

* Fault Tolerance
* Scalability
* Performance

### Distributed Systems Difficulties

* Network Failure
* Latency
* Observability
* Management & Overhead

### Types of Distributed Systems

Distributed systems generally fall into one of four different basic architecture models:

1. **Client-Server** - Clients contact the server for data, then format it and display it to the end-user. The end-user can also make a change from the client-side and commit it back to the server to make it permanent.
2. **Three-Tier** - Information about the client is stored in a middle tier rather than on the client to simplify application deployment. This architecture model is most common for web applications.
3. **n-Tier** - Generally used when an application or server needs to forward requests to additional enterprise services on the network
4. **Peer-to-Peer** - There are no additional machines used to provide services or manage resources.  Responsibilities are uniformly distributed among machines in the system, know as peers, which can serve as either client or server.

