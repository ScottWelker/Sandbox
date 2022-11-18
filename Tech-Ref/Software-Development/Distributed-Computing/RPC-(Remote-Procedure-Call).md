[Home](/Slalom-LLC/Slalom-Consulting) | [Glossary](/Glossary) | [Tech Ref](/Tech-Ref) | [DevOps](/Tech-Ref/Software-Development/DevOps-\(Development-and-IT-Operations\)) | [Software Development](/Tech-Ref/Software-Development) | [Distributed Computing](/Tech-Ref/Software-Development/Distributed-Computing)

[[_TOC_]]

---
# Introduction
"_In [distributed computing](/Tech-Ref/Software-Development/Distributed-Computing), a ***Remote Procedure Call (RPC)*** is when a computer program causes a procedure (subroutine) to execute in a different address space (commonly on another computer on a shared network), which is coded as if it were a normal (local) procedure call, without the programmer explicitly coding the details for the remote interaction. That is, the programmer writes essentially the same code whether the subroutine is local to the executing program, or remote. This is a form of client–server interaction (caller is client, executor is server), typically implemented via a request–response message-passing system. In the object-oriented programming paradigm, RPCs are represented by [remote method invocation (RMI)](/Tech-Ref/Software-Development/Java/Java-Platform-Editions/Java-SE-\(Standard-Edition\)/RMI-\(Remote-Method-Invocation\)). The RPC model implies a level of location transparency, namely that calling procedures are largely the same whether they are local or remote, but usually they are not identical, so local calls can be distinguished from remote calls. Remote calls are usually orders of magnitude slower and less reliable than local calls, so distinguishing them is important._"

"_RPCs are a form of inter-process communication (IPC), in that different processes have different address spaces: if on the same [host](/Tech-Ref/Networking/Host) machine, they have distinct virtual address spaces, even though the physical address space is the same; while if they are on different [hosts](/Tech-Ref/Networking/Host), the physical address space is different. Many different (often incompatible) technologies have been used to implement the concept._"

## Reference
1. [Wikipedia: https://en.wikipedia.org/wiki/Remote_procedure_call](https://en.wikipedia.org/wiki/Remote_procedure_call)

---
# Topics
1. [Distributed Computing](/Tech-Ref/Software-Development/Distributed-Computing).
1. [RMI (Remote Method Invocation)](/Tech-Ref/Software-Development/Java/Java-Platform-Editions/Java-SE-\(Standard-Edition\)/RMI-\(Remote-Method-Invocation\)) - [Java](/Tech-Ref/Software-Development/Java).
1. [Spring Framework](/Tech-Ref/Software-Development/Java/Java-Platform-Editions/Jakarta-EE-\(Enterprise-Edition\)/Spring-Framework) / [Spring Boot](/Tech-Ref/Software-Development/Java/Java-Platform-Editions/Jakarta-EE-\(Enterprise-Edition\)/Spring-Framework/Spring-Boot).
