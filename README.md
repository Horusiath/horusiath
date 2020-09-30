### Hi there 👋

My name is Bartosz Sypytkowski. I'm a passionate distributed systems developer, interested in internals, protocol and algorithms driving such systems. You can see some of the recent topics of my interest on my [blog post](https://bartoszsypytkowski.com/). 

While I look at the platform/runtime as a tool to achieve the goal, my personal preferences include: Rust, Scala, F#, Go.

From time to time I manage to speak at user groups and conferences. Your can see some of my presentations on youtbute and in [slideshare](https://www.slideshare.net/BartoszSypytkowski1/presentations).

### Hall of fame

During my carrier I worked in open source over several different open source projects:

- [Akka.NET](https://getakka.net/) - over 5 years I contributed by building a various parts of this distributed actor framework, including:
    - [Akka.Streams](https://github.com/akkadotnet/akka.net/pull/1727), which is a reactive streaming library build on top of akka actors, that allows programmers to build a rich dataflow graphs with backpressure support. This also included building a direct API for safe and composable socker server and client as well as [StreamRefs](https://github.com/akkadotnet/akka.net/pull/3321) - an ability to transport and join Akka.Streams graph nodes over the network, allowing users to build a distributed, backpressured dataflows.
    - [Akka.Persistence](https://github.com/akkadotnet/akka.net/pull/577) which is an actor plugin, that introduces support to actor state persistence by using eventsourcing techniques. Later on I also introduced Akka.Streams support to it as well as SQL database adapters. 
    - [Akka.DistributedData](https://github.com/akkadotnet/akka.net/pull/2261) which introduced a decentralized, replicated in-memory key-value store build into akka cluster, based on Conflict-free Replicated Data Types. Later on it was extended to use optimized [delta-state](https://github.com/akkadotnet/akka.net/pull/2749) CRDTs and [durable storage](https://github.com/akkadotnet/akka.net/pull/2490).
    - [Akka.Cluster.Sharding](https://github.com/akkadotnet/akka.net/pull/1502) which enabled automatic shard-based actor placement, with rebalancing strategy that enabled efficient cluster resource utilization.
    - [Support for mutli-datacenter aware clusters](https://github.com/akkadotnet/akka.net/pull/3284)
    - [Cluster split brain resolution strategy](https://github.com/akkadotnet/akka.net/pull/3180), which was reverse engineered from canonical Akka JVM documentation (it was not open-sourced back then).
    - [Akka.Persistence.Reminders](https://github.com/Horusiath/Akka.Persistence.Reminders) which extended eventsourced capabilities of Akka.Persistence to support long-running timers. It also included support to cron expressions.
    - [Akka.Cluster.Discovery](https://github.com/Horusiath/Akka.Cluster.Discovery) which is node-discovery service, that enables to use 3rd party systems (like Hashicorp Consul) to mediate in akka cluster initialization.
    - [F# pluggin for Akka](https://www.nuget.org/packages/Akkling/)
- [FSharp.Data.GraphQL](https://fsprojects.github.io/FSharp.Data.GraphQL/) which is Bazinga Inc. sponsored project, where I implemented a server-side part of GraphQL standard specification. Some of the more interesting challenges was to implement GraphQL-to-LINQ converter, that was using not only GraphQL query AST, but actually tracket usage of data types in underlying F# code used in field resolvers.
- [Hyperion](https://github.com/akkadotnet/Hyperion) which is a very efficient binary serializer, aiming to provide a wide features support eg. serialization of object graphs with cycles, serialization of expressions and delegates, version tolerance.