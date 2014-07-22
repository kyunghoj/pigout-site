---
layout: page
permalink: /overview/
title: "PigOut Overview"
modified: 2014-07-21 18:40
tags: [Overview]
---

## Motivation

Hadoop has gained tremendous traction from both academica and industry
since its release, having been widely adopted by industry and inspiring
numerous publications in acadmic conferences and journals in the past
few years. 

Due in part to Hadoop's ease of use and management,
even relatively small organizations or departments are spinning
up Hadoop infrastructures for internal use. This proliferation
of Hadoop instances is driving a need for federated (i.e.,
inter-cluster) functionality to support multi-organization coalitions,
collaborations across different administrative domains
within a single organization, or even collaboration between on-site
clusters and infrastructures deployed on cloud-computing
backends. Workflow systems such as Oozie, Pegasus, and Kepler
provide support for inter-cluster workflows. However, fixed
workflows make it hard to adapt to changing cloud pricing
schemes, resource availability, organizational policies, and
international laws. In short, creating multi-cluster workflows
is still quite hard.

PigOut enables multiple Hadoop clusters to work together. PigOut addresses
two main challenges critical for multi-cluster support:
**ease of programming** and **ease of management**.

### Easy Programming

PigOut achieves ease of programming by leveraging Pig, a popular system in
Hadoop ecosystem. Pig provides a high-level language, Pig Latin, for data
processing and a runtime that generates a series of MapReduce jobs from a
script written in Pig Latin. 
Writing a Pig Latin script is easier than writing native MapReduce
applications, which makes it a popular choice among developers and data
analysts. PigOut essentially extends this benefit of Pig to federated
clusters by automatically partitioning individual Pig Latin scripts for
execution on different clusters. From the developer's point of
view, there is little difference between writing a script for a
single cluster and multiple cluster

### Easy Management

PigOut is a front-end that interfaces with multiple Hadoop clusters. 
It does not require any change to existing infrastructures. This is
possible because PigOut partitions scripts into complete stand-alone 
Pig Latin scripts, each independently runnable on a Hadoop cluster. 
From a cluster administrator's point of view, there is no difference
in supporting and running a regular Pig script and a PigOut script.
