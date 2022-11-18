[Home](/Slalom-LLC/Slalom-Consulting) | [Glossary](/Glossary) | [Tech Ref](/Tech-Ref) | [.NET](/Tech-Ref/Software-Development/NET-Framework) | [Software Development](/Tech-Ref/Software-Development) | [C#](/Tech-Ref/Software-Development/CSharp)

[[_TOC_]]

---
# Introduction
"_***Thread Starvation*** are cases where tasks dispatched to managed [thread pool](/Tech-Ref/Software-Development/CSharp/Thread-Pool-\(CSharp\)) don't start executing immediately due to other work in the [thread pool](/Tech-Ref/Software-Development/CSharp/Thread-Pool-\(CSharp\)). In certain cases, the starvation can cause task execution to delay up to a second and if the main thread is waiting for the task to complete, this will cause elapsed time regressions as well as responsiveness issues in the product._"

"_A thread pool starvation issue usually manifests itself as a long blocked time on main thread waiting for background work._"

## Reference
1. [Investigating thread starvation issues](https://github.com/microsoft/vs-threading/blob/main/doc/threadpool_starvation.md)

---
# Topics
1. [.NET Framework](/Tech-Ref/Software-Development/NET-Framework).
1. [C# (CSharp)](/Tech-Ref/Software-Development/CSharp).
1. [Resiliency Team (CAI)](/Clients/CAI-\(Cox-Automotive-Inc\)/Resiliency-Team-\(CAI\)).
1. [Thread Pool (CSharp)](/Tech-Ref/Software-Development/CSharp/Thread-Pool-\(CSharp\)).
