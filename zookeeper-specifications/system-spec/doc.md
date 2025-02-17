# ZooKeeper's System Specification of TLA+

## Overview

ZooKeeper's system specification of TLA+ focuses on the implementation of the Zookeeper Atomic Broadcast(ZAB) consensus protocol (or, [ZAB1.0](https://cwiki.apache.org/confluence/display/ZOOKEEPER/Zab1.0)). 

As is shown by the informal description of [ZAB1.0](https://cwiki.apache.org/confluence/display/ZOOKEEPER/Zab1.0), the implementation of ZAB that used in ZooKeeper production differs a lot from its original design.

We make this system specification to grasp the core logic of the ZAB's implementation especially. 

The [sysetm specification](zk-3.7/ZkV3_7_0.tla) written in TLA+ is precise without ambiguity, and testable with existed tools like the TLC model checker. (We have done a certain scale of model checking to verify its correctness!) 

The system specification can serve as the super-doc supplementing detailed system documentation for the ZooKeeper developers. It can evolve incrementally without high cost as the system develops over time, continually ensuring correctness for both the design and the implementation.

We have also made a formal [specification](zk-3.7/FastLeaderElection.tla) for Fast Leader Election in Zab since ZAB 1.0 depends on FLE to complete the election phase.

If you have any question or find any problem of the specification, please contact us.
