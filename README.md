### Hi there 👋

My name is Bartosz Sypytkowski. I'm a passionate about data management, distributed & concurrent systems, their internals, protocols and algorithms driving them. You can see some of the recent topics of my interest on my [blog post](https://bartoszsypytkowski.com/). Some of my personal favourites:

- Series of posts introducting to [Conflict-free Replicated Data Types](https://bartoszsypytkowski.com/tag/crdt/).
- Walkthrough (with implementation) over [SWIM](https://bartoszsypytkowski.com/make-your-cluster-swim/) and [HyParView](https://bartoszsypytkowski.com/hyparview/) cluster membership protocols.
- [Post](https://bartoszsypytkowski.com/building-custom-fibers-library-in-f/) about tradeoffs and building custom user-space threads in F#.
- [How to build custom thread-per-core thread pool](https://bartoszsypytkowski.com/thread-safety-with-affine-thread-pools/).
- [How to build custom actor library](https://bartoszsypytkowski.com/build-your-own-actor-model/).
- A bunch of tips related to [CPU/memory optimization](https://bartoszsypytkowski.com/writing-high-performance-f-code/) of .NET programs from F# developer point of view.
- How to build [async-aware Read/Write lock](https://bartoszsypytkowski.com/async-rwlock/) operating in user space over .NET green thread model (Tasks).
- How to build [Range tries](https://bartoszsypytkowski.com/r-tree/): data structures used for efficient indexing of multi-dimensional data.

While I look at the platform/runtime as a tool to achieve the goal, my personal weapons of choice include: Rust (which I had pleasure to work with when implementing JSON-like CRDT document database at [ditto.live](https://ditto.live)), Scala, F#, Go.

From time to time I manage to speak at user groups and conferences. Your can see some of my presentations on youtube and [slideshare](https://www.slideshare.net/BartoszSypytkowski1/presentations). Feel free to contact me (you can see e-email in my github profile). 

### Hall of fame

Some of the open source projects I contributed to:

- [Yrs](https://github.com/y-crdt/y-crdt) - it's a Rust implementation of Yjs library (one of the most performant CRDT libraries for building rich collaborative documents), targetting multi-platform systems and serving as foundation for multiple language bindings including Web Assembly, C FFI, Python or Ruby.
- [Akka.NET](https://getakka.net/) - for over 5 years I was member of core-team, where I helped building a various parts of this distributed actor framework, including:
    - [Akka.Streams](https://github.com/akkadotnet/akka.net/pull/1727), which is a reactive streaming library build on top of akka actors, that allows programmers to build a rich dataflow graphs with backpressure support. This also included building a direct API for safe and composable socker server and client as well as [StreamRefs](https://github.com/akkadotnet/akka.net/pull/3321) - surrogate objects used to transport and join Akka.Streams graph nodes over the network, allowing users to build a distributed, backpressured dataflows.
    - [Akka.Persistence](https://github.com/akkadotnet/akka.net/pull/577) which is a plugin, that introduces support to actor state persistence by using eventsourcing techniques. Later on I also introduced Akka.Streams support to it as well as SQL database adapters.
    - [Akka.DistributedData](https://github.com/akkadotnet/akka.net/pull/2261) which introduced a decentralized, replicated in-memory key-value store build into akka cluster, based on Conflict-free Replicated Data Types. Later on it was extended to use optimized [delta-state](https://github.com/akkadotnet/akka.net/pull/2749) CRDTs and [durable storage](https://github.com/akkadotnet/akka.net/pull/2490).
    - [Akka.Cluster.Sharding](https://github.com/akkadotnet/akka.net/pull/1502) which enabled automatic shard-based actor placement, with rebalancing strategy that enabled efficient cluster resource utilization.
    - [Cluster split brain resolution strategy](https://github.com/akkadotnet/akka.net/pull/3180), which was reverse engineered from canonical Akka JVM documentation (it was not open-sourced back then).
    - [Akka.Persistence.Reminders](https://github.com/Horusiath/Akka.Persistence.Reminders) which extended eventsourced capabilities of Akka.Persistence to support long-running timers. It also included support to cron expressions.
    - [Akka.Cluster.Discovery](https://github.com/Horusiath/Akka.Cluster.Discovery) which is a node-discovery service, that enables to use 3rd party systems (like Hashicorp Consul) to mediate in akka cluster initialization.
    - [F# pluggin for Akka](https://www.nuget.org/packages/Akkling/)
    - [Support for mutli-datacenter aware clusters](https://github.com/akkadotnet/akka.net/pull/3284)
    - [Second shot to eventsourcing](https://github.com/Horusiath/Eventuate.NET) with support to replicated partially ordered event log - based on [eventuate](https://rbmhtechnology.github.io/eventuate/) Akka library.
- [FSharp.Data.GraphQL](https://fsprojects.github.io/FSharp.Data.GraphQL/) which is Bazinga Inc. sponsored project, where I implemented a server-side part of GraphQL standard specification. Memorable challenge was to implement GraphQL-to-LINQ converter, that was using not only GraphQL query AST, but actually tracked usage of data members in underlying F# code used in field resolvers.
- [Hyperion](https://github.com/akkadotnet/Hyperion) which is a very efficient binary serializer, aiming to provide a wide features support eg. serialization of object graphs with cycles, serialization of expressions and delegates, version tolerance.
- A growing collection of various [Conflict-free Replicated Data Types](https://github.com/Horusiath/crdt-examples), including state-, delta-state and operation-based ones (with example replication protocol support).
- [A F# utility library](https://github.com/horusiath/fsharp.core.extensions), with various extensions like high performance persistent vectors, hybrid-logical clocks, reentrant user-space read/write locks, set of operators over IAsyncEnumerable interaface or high performance actor implementation.
