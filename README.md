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

Visit the [Mastermnd Academy](https://academy.mastermnd.io/journeys/pipelines/) website for more information

## DevOps/SRE Review

2020-05-09

Notes were not taken as this was a review of the Intro to DevOps course.  Refer to the previous 24 part course.


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

### AWS Setup at this point

Instances are based on RHEL.

* nginx instance for reverse proxy
* gatsby/nginx instance for site host
* fulcrum instance
* rocket-chat instance
* bastion host instance
* vpc with 1 public 1 private subnet
* igw pointed to route table
* sg's with open ports for public subnet

## Development & Delivery Strategy

2020-05-23

### Software Development Lifecycle

A process for planning, creating, testing, and deploying an information systems.  The systems development life cycle concept applies to a range of hardware and software configurations, as a system can be composed of hardware only, software only, or a combination of both. There are usually six stages in this cycle: requirements analysis, design, development and testing, implementation, documentation, and evaluation.

#### Requirements Analysis

* Determine user expectations for a new or modified product.
* Feasibility Study.
* Requirements Gathering.
* Software Specification.
* Negotiation & Discussion.
* Documentation.

#### Design

* Software design is the process of envisioning and defining software solutions to one or more set of problems.
* Software Architecture.
* UX/UI.
* Graphic.

#### Development

* Gametime!
* Developing the code to achieve the requirements.

#### Testing

* How we know our code is doing what we intended it to.
* Unit - testing a single unit/part of the code.
* Integration - testing units/parts are working together.
* End to End - testing the entire application.

#### Implementation(Deployment)

* Get the product into the users' hands.
* Collect feedback metrics.

#### Documentation

* Application usage.
* Software.
* Architecture.
* Processes.

#### Evaluation

* Did the solution actually work?

### What is Git?

#### Git

Git is a distributed version control systems for tracking changes in source code during software development. It is designed for coordinating work among programmers, but it can be used to track changes in any set of files. Its goals include speed, data integrity, and support for distributed, non-linear workflows.

#### What the heck does that mean?

- There is no central version of a codebase.  Each user has a working copy and the full change history.
- Tracks changes to a codebase and exchanges patches when codebase needs to be synchronized.

### What is a Git Repository?

#### Our Code Needs a Home!

Git Repositories store metadata for sets of files and/or directories. It stores the set of files as well as history of changes made to those files.

#### Git Branches

Like a branch of a tree, a code branch is connectewd to the trunk, but is free to grow off in a it's own direction.

#### War of the Repositories

| GitHub | GitLab | BitBucket |
|--------|--------|-----------|
| Acquired by Microsoft | More than just SCM | Atlassian product means good integration with other Atlassian products |
| Largest Market Share | Project Planning | Built-in CI |
| Unlimited Free Public and Private Repos (Private repos limited to only 3 collaborators) | CI/CD Pipeline | Unlimited Public and Private Repos |
| | Monitoring | |
| | Metrics | |
| | Unlimited Public and Private Repos | |

