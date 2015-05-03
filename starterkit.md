---
layout: page
title: Starter Kit
permalink: /starterkit/
---

# Concepts

There are three different types of computer processing: Batch Processing, Online Processing and Real-time Processing.

**Batch processing** is an efficient way of processing high volumes of data is where a group of transactions is collected over a period of time. Data is collected, entered, processed and then the batch results are produced (Hadoop is a main example). Typically used on billing process or non real time task.

**Online processing** processes information when it is received and performs data processing instantly. This type of processing is set to processes where there is an iteration by external systems for example online commerce transactions.

**Real-time processing** involves a continual input, process and output of data. Data must be processed in a small time period (or near real time). 

## Real-Time Processing

MapReduce, Hadoop, and related technologies have made it possible to store and process data at scales previously unthinkable. Unfortunately, these data processing technologies are not real time systems. There's no way that will turn Hadoop into a real time system.

In a nutshell these are the main differences between Hadoop and Storm:

| **Hadoop**                | **Storm**         |
| :---------------------: |:-------------:| 
| Large but finite jobs | Infinite computations called Topologies |
| Processes a lot of data at once | Process Infinite streams of data one tuple at a time  |
| High Latency          | Low Latency |

However, real time data processing at massive scale is becoming more and more of a requirement for businesses and definitely for Security industry.

Nowadays data generating is increasing. Real time processing is needed to get this information and determine if an action is required. In a security point of view, these data contains potential information which may involve a potential risk, so it is necessary to be able to detect it early.

New framework implements new paradigms are needed. Key properties of this type of solutions should be:

1. **Extremely broad set of use cases**: It should be used for processing messages and updating databases (stream processing), doing a continuous query on data streams and streaming the results into clients (continuous computation), parallelizing an intense query like a search query on the fly (distributed RPC), and more.

2. **Scalable**: It should be scale to massive numbers of messages per second.

3. **Guarantees no data loss**: A realtime system must have strong guarantees about data being successfully processed. A system that drops data has a very limited set of use cases.
 
4. **Extremely robust**: It should be simple manage.

5. **Fault-tolerant**: If there are faults during execution of your computation, system will reassign tasks as necessary. System should make sure that a computation must run forever (or until you kill the computation).

6. **Programming language agnostic**: Robust and scalable realtime processing shouldn't be limited to a single platform. 


## Storm

> Apache Storm is a free and open source distributed real time computation system. 
> Storm is simple, can be used with any programming language. It is scalable, fault-tolerant, guarantees your data will be processed, and is easy to set up and operate.

Originated at Backtype, acquired by Twitter in 2011. Storm become Open Source late 2011 and was part of Apache Incubator late 2013. Today Storm is top level Apache project.

<image>

Storm is a platform for perform analysis on streams of data (continuous data flows) as they receive or collect, enabling information processing as it happens.

Storm has many use cases: real time analytics, online machine learning, continuous computation, distributed RPC, ETL, and more. Storm is able to integrates with the queueing and database technologies you already use is your systems.

Currently the trend indicates the potential of this technology in the Real Time processing paradigm.

<image>

### Storm main concepts

Storms use Stream concept, seen a stream as an unbounded sequence of tuples. Every stream has an “id”. Stream is defined with a schema that names the fields in the tuple. Tuples values must be serializable.
