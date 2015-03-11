# Config Mgmt Strategy

At this time, configuration management (CM) code is a community "best effort" initiative. Maintaining these repositories that are useful for Riak configuration will require a combination of clear guidelines and community collaboration. 

Here's where we think we're starting and some direction on where we go. We'd love for you to be part of the process.


### What we mean by Configuration Management

Some tools, often run by Ops to enable Dev and spoken about as "DevOps", used in conjunction with Riak to install and configure Riak include [Chef](https://www.chef.io/), [Puppet](https://puppetlabs.com/) and [Ansible](http://www.ansible.com/). We (at Basho) see the automation and orchestration available through these products as core to infrastructure today.


### Our Goal [Very Beta - Open PRs to Discuss]

We'd like to have a single system for all tools that tells you, the community member, how much Riak functionality is available by using it. Each toolset has its own terms and best practices. That's fine. What we would like to achieve is a common ground for definitions of Riak's functions in relation to these tools. 

We'll call each code base's compliance a **Riak automation levels** (RAL). RALs will have different levels that are clearly defined below as either **Basic**, **Intermediate** or **Advanaced**. RALs will be defined for each tool and each functional requirement.


### Riak Automation Levels Status


| Tool | Requirement | RAL Level | Last Tested |
|:----:|-------------|:---------:|-------------|
|
|
|


## Riak Installation Requirements

### Basic

* Version

    * Hardcoded

    * Allow Custom 

    * OSS only

* Install Location - Package Default

### Intermediate

* Version

    * Latest

    * Riak EE (be able to download from S3 using a URL code)

### Advanced

* Location - Custom

* Basho Patches (Folder : basho-patches - check for any patches released after the release and install those or at least provide recommendations on e.g. optimal Erlang and additional CM elements to support that)

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

* Leave Cluster

* Rolling Restart

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

