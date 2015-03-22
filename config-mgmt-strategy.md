# Config Mgmt Strategy

At this time, configuration management (CM) code is a community "best effort" initiative. Maintaining these repositories that are useful for Riak configuration will require a combination of clear guidelines and community collaboration. 

Here's where we think we're starting and some direction on where we go. We'd love for you to be part of the process.


### What we mean by Configuration Management

Some tools, often run by Ops to enable Dev and spoken about as "DevOps", used in conjunction with Riak to install and configure Riak include [Chef](https://www.chef.io/), [Puppet](https://puppetlabs.com/) and [Ansible](http://www.ansible.com/). We (at Basho) see the automation and orchestration available through these products as core to infrastructure today.


### Our Goal [Very Beta - Open PRs to Discuss]

We'd like to have a single system for all tools that tells you, the community member, how much Riak functionality is available by using it. Each toolset has its own terms and best practices. That's fine. What we would like to achieve is a common ground for definitions of Riak's functions in relation to these tools.

We'll call each code base's compliance a **Riak management level** (RML). RMLs will have different levels that are clearly defined below as either **Basic**, **Intermediate** or **Advanced**. RMLs will be defined for each tool and each functional requirement.


### Riak Management Levels Status


| Tool         |  Requirement  | RML Level | Last Tested |
|:--------:    |---------------|:---------:|-------------|
|**Ansible**   |Installation   |
|              |Configuration  |
|              |Data Operation |
|              |Services       |
|              |MDC Operation  |
|              |Code Quality   |
|              |               |
|**Puppet**    |Installation   |
|              |Configuration  |
|              |Data Operation |
|              |Services       |
|              |MDC Operation  |
|              |Code Quality   |
|              |               |
|**Chef**      |Installation   |
|              |Configuration  |
|              |Data Operation |
|              |Services       |
|              |MDC Operation  |
|              |Code Quality   |


## Riak Installation Requirements

### Basic

* Version

    * Hardcoded

    * Allow Custom package name

    * OSS only

* Install Location - Package Default

### Intermediate

* Version

    * Latest

    * Riak EE (be able to download from S3 using a URL code)

### Advanced

* Location - Custom

* Version - Git / Source

## Riak Configuration Requirements

### Basic

* Options in riak.conf

    * Node Name

    * Listen Address & Port

    * Ring Size

    * Distributed Cookie

    * Solr on/off

* Custom riak.conf Template (include their own but change the node name, addresses etc)

### Intermediate

* Options in riak.conf

    * AAE (On/Off)

    * SSL

    * Multi-Backend

    * Disk Locations

* Include custom advanced.config

### Advanced

* Options in riak.conf

    * All Options

* Riak EE Options

    * All Options

Note: Leverage OS level configuration options available with the CM tools to tune the OS

## Riak Data Operations Requirements

### Basic

* Bucket

    * Set Props from JSON

* Bucket Types

    * Create from JSON

    * Activate

* Solr

    * Create Index

### Intermediate

* Bucket

    * Set Props via API

        * n_val

        * allow_mult

        * search_index

* Solr

    * Create Index using Schema

    * Add Schema

### Advanced

* Secondary Indexes

* Bucket Properties

    * Quorum

    * Hooks

* Bucket Types

    * API for CRDT Types

    * Update

* Security

    * Enable & Configure

* Strong Consistancy

    * Enable & Configure

## Riak Service Requirements

### Basic

* Start/Stop Service

## Riak Cluster Operations Requirements

### Basic

* Join Cluster

### Intermediate

* Discover existing cluster using CM-native tooling

* Leave Cluster

* Rolling Restart

### Advanced

* Bootstrap full cluster with no manual configuration steps

* Group changes to multiple nodes and make one staged cluster plan to avoid unnecessary rebalancing

* Provide ability to block cluster changes if rebalancing is already underway

## Riak Multi Data Center Operations

### Basic

* MDC v3

    * Set Cluster Name

### Intermediate

* MDC v3

    * Configure Address & Port

    * Connect

    * Realtime

        * Enable / Disable

        * Start / Stop

    * Full Sync

        * Enable / Disable

        * Start / Stop

        * Configure Scheduling

### Advanced

* MDC v3

    * Realtime Cascade

    * NAT

    * Tuning

## Code Quality

### Basic

* Example executable code

* Automated tooling (rake, make, etc) to run:

  * Linting on core config management code

  * Any unit testing at all

* Documentation or metadata should list supported platforms

* Licensed with an OSI-approved open source license

* Code is idempotent and fully converges in one run, unless technical limitations in the tooling or underlying software prevent it

### Intermediate

* Code is versioned using semver

* Automated tooling (rake, make, etc) to run:

  * Linting on config management code as well as validating any JSON, YAML, config files, etc.

  * Unit tests and/or VM-based integration tests (e.g. Beaker or Test Kitchen) with test coverage for major functionality

* Publicly accessible CI system that runs linting and some level of unit and/or acceptance tests on pull requests prior to merges

* All functionality implemented using abstractions native to the configuration management tool, not exec or similar

* Where possible, code defaults to installing all software via system package management tools using package repositories

* No manual steps needed to install any dependencies or configuration files before running CM tool

### Advanced

* Publicly accessible CI infrastructure that runs both unit tests and acceptance tests for all supported platforms

* If the configuration management tool has a ratings or approval system for modules, it should be approved. (e.g. Puppet Approved forge modules)
