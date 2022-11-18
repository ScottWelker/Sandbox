[Home](/Slalom-LLC/Slalom-Consulting) | [Glossary](/Glossary) | [Tech Ref](/Tech-Ref) | [.NET](/Tech-Ref/Software-Development/NET-Framework) | [Software Development](/Tech-Ref/Software-Development) | [C#](/Tech-Ref/Software-Development/CSharp)

[[_TOC_]]

---
# Introduction
"The managed _***Thread Pool*** provides your application with a pool of worker threads that are managed by the system, allowing you to concentrate on application tasks rather than thread management. If you have <mark>short tasks</mark> that require background processing, the managed thread pool is an easy way to take advantage of multiple threads._"

## Reference
1. [Docs.Microsoft: The managed thread pool](https://docs.microsoft.com/en-us/dotnet/standard/threading/the-managed-thread-pool)
1. [C-SharpCorner: Thread Pooling in C#](https://www.c-sharpcorner.com/UploadFile/1d42da/threading-pooling-in-C-Sharp/).

## Notes
1. Use of the thread pool is significantly easier in Framework 4 and later, since you can create `Task` and `Task<TResult>` objects that perform asynchronous tasks on thread pool threads.
1. Thread pool threads are [background](https://docs.microsoft.com/en-us/dotnet/standard/threading/foreground-and-background-threads) threads.
1. Once a thread in the thread pool completes its task, it's returned to a queue of waiting threads. From this moment it can be reused. This reuse enables applications to avoid the cost of creating a new thread for each task.
1. There is only one thread pool per process.
1. If all thread pool threads are busy, additional work items are queued until threads to execute them become available.

---
# Topics
1. [.NET Framework](/Tech-Ref/Software-Development/NET-Framework).
1. [C# (CSharp)](/Tech-Ref/Software-Development/CSharp).
1. [Resiliency Team (CAI)](/Clients/CAI-\(Cox-Automotive-Inc\)/Resiliency-Team-\(CAI\)).
1. [Software Development](/Tech-Ref/Software-Development).
1. [Visual Studio](/Tech-Ref/Microsoft/Visual-Studio).

---
# When NOT to use thread pool threads
- [When not to use thread pool threads](https://docs.microsoft.com/en-us/dotnet/standard/threading/the-managed-thread-pool#when-not-to-use-thread-pool-threads):
   - :+1: <mark>You have tasks that cause the thread to block for long periods of time.</mark>
