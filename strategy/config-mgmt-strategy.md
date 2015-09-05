# Config Mgmt Strategy

At this time, configuration management (CM) code is a community "best effort" initiative. Maintaining these repositories that are useful for Basho product configuration will require a combination of clear guidelines and community collaboration. 

Here's where we think we're starting and some direction on where we go. We'd love for you to be part of the process.


### What we mean by Configuration Management

Configuration management tools install packages, manage configuration files, control services, and otherwise define infrastructure state using code.
These tools simplify installation and management of Riak. The basho-labs project includes code for managing Riak using [Chef](https://www.chef.io/), [Puppet](https://puppetlabs.com/) and [Ansible](http://www.ansible.com/). We (at Basho) see the automation and orchestration available through these products as core to infrastructure today.


### Our Goal [Beta - Open PRs or Issues to Discuss]

We're starting with a focus on just Riak KV, our distributed database.

We'd like to have a single system for all tools that tells you, the community member, how much Riak KV functionality is available by using it. Each toolset has its own terms and best practices. That's fine. What we would like to achieve is a common ground for definitions of Riak's functions in relation to these tools.

We'll call each code base's compliance a **Riak management level** (RML). RMLs will have different levels that are clearly defined below as either **Basic**, **Intermediate** or **Advanced**. RMLs will be defined for each tool and each functional requirement.

### Community Supported Repos
Here are the three repositories monitored by @mjbrender from the Developer Advocacy team. You can add other helpful repos that should be kept in consideration here.

* **Chef** = https://github.com/basho-labs/riak-chef-cookbook
* **Ansible** = https://github.com/basho-labs/ansible-riak
* **Puppet** = https://github.com/basho-labs/puppet-riak


### Configuration Tool Riak Management Capabilities

| Tool              | **Ansible**   | **Puppet**   | **Chef** |
|-------------------|---------------|--------------|--------|
| **Status**
| Public CI Status  | ????          | [![Build Status](https://travis-ci.org/basho-labs/puppet-riak.svg?branch=master)](https://travis-ci.org/basho-labs/puppet-riak) | [![Build Status](https://travis-ci.org/basho-labs/riak-chef-cookbook.svg?branch=master)](https://travis-ci.org/basho-labs/riak-chef-cookbook)
| Latest Release    | ???           | [![PuppetForge](http://img.shields.io/puppetforge/v/basholabs/riak.svg?style=flat-square)](https://forge.puppetlabs.com/garethr/docker) | [![Cookbook Version](http://img.shields.io/cookbook/v/riak.svg)](https://supermarket.getchef.com/cookbooks/riak) |
| License           | Apache-2.0    | Apache-2.0   | Apache-2.0
| **Versions**
| Supports Riak 1.x | yes           | no           | yes 
| Supports Riak 2.x | no            | yes          | yes
| Tool Version Requirement | ???    | Puppet 3.7+  | Chef 11
| **Installation** 
| System packages   | yes           | yes          | yes
| Riak EE S3 download | yes(?)      | no           | yes
| Ad-hoc patches      | yes(???)    | no           | yes
| **Configuration**
| riak.conf         | all settings  | all settings | all settings
| advanced.conf     | no           | no           | no (?)
| OS performance settings | ???     | no           | yes
| **Management**
| Create buckets    | ???           | no           | no
| Alter buckets     | ???           | no           | no
| Create solr index | ???           | no           | no
| Create solr index using schema | ??? | no        | no
| Add solr schema   | ???           | no           | no
| Manage secondary indexes | ???    | no           | no
| Set bucket properties | ???       | no           | no
| Enable security   | ???           | no           | ???
| Manage security   | ???           | no           | ???
| Enable strong consistency | ???   | no           | ???
| Manage strong consistency | ???   | no           | ???
| Data Operation    | Intermediate? | no           | no
| **Cluster Management**
| Join Cluster     | yes (?)       | no           | no
| Discover Cluster | ???            | no           | no
| Leave Cluster    | ???            | no           | no
| Rolling Restart  | ???            | no           | no
| hands-off bootstrap | no | no     | no           | no
| stage changes     | no            | no           | no
| **Multi-Datacenter** (Riak EE only)
| Set Cluster Name  | ???           | no (?)       | no (?)
| Connect           | ???           | no (?)       | no (?)
| Sync              | ???           | no (?)       | no (?)
| Configure Scheduling | ???        | no (?)       | no (?)
| Realtime Cascade  | ???           | no (?)       | no (?)
| NAT               | ???           | no (?)       | no (?)
| Performance Tuning| ???           | no (?)       | no (?)
| **Code Quality** 
| Unit tests        | ????          | yes          | yes
| VM-based Integration Tests | ???? | yes (beaker) | yes (test kitchen)


## Riak Installation Requirements

### Basic

* Version

    * Latest (Hardcoded)

    * Start/stop service

    * OSS only

* Install Location - Package Default

### Intermediate

* Version

    * Latest by default, configurable

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
