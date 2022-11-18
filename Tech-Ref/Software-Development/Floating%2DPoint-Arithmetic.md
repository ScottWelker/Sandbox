[Home](/Slalom-LLC/Slalom-Consulting) | [Glossary](/Glossary) | [Tech Ref](/Tech-Ref) | [Software Development](/Tech-Ref/Software-Development) | [DevOps](/Tech-Ref/Software-Development/DevOps-\(Development-and-IT-Operations\))

[[_TOC_]]

---
# Introduction

Try the following in your programming language of choice. You may be surprised by the result:

```
.1 + .2 = .3
```

You will usually get `false`. See [Examples](#Examples) below. 

## Reference
1. [What Every Computer Scientist Should Know About Floating-Point Arithmetic](https://docs.oracle.com/cd/E19957-01/806-3568/ncg_goldberg.html)
1. [IEEE Standard for Floating-Point Arithmetic (IEEE 754)](https://en.wikipedia.org/wiki/IEEE_754)
1. [Floating-point arithmetic](https://en.wikipedia.org/wiki/Floating-point_arithmetic)
   - [Accuracy problems](https://en.wikipedia.org/wiki/Floating-point_arithmetic#Accuracy_problems)
1. [Floating-point numeric types (C# reference)](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types)
1. [Decimal data type](https://en.wikipedia.org/wiki/Decimal_data_type)

---
# Topics
1. [C#](/Tech-Ref/Software-Development/CSharp).
1. [Java](/Tech-Ref/Software-Development/Java).
1. [JavaScript](/Tech-Ref/Software-Development/JavaScript).
1. [PowerShell](/Tech-Ref/Microsoft/PowerShell).
1. [Python](/Tech-Ref/Software-Development/Python).
1. [Software Development](/Tech-Ref/Software-Development).

---
# Examples

## Windows Batch/Cmd Script
Not applicable. Windows batch files don't support floating-point arithmetic. 
- [Windows batch... does not support floating-point arithmetic](https://stackoverflow.com/a/1869218/418950)
- :+1: There are techniques with which to simulate floating point values and arithmetic. However, if you need to do that then [I (SWelker)](/Individuals/Scott-Welker) believe bat/cmd scripting just isn't the right approach.

## C# (CSharp)
This [C#](/Tech-Ref/Software-Development/CSharp) console application example omits the "_scaffolding_", `static void Main(string[] args)` , and shows just the output.

```csharp
Console.WriteLine(.1 + .2 == .3);
```
Output is:
```
False
```

## Java
This [Java](/Tech-Ref/Software-Development/Java) example omits the "_scaffolding_", `public static void main(String[] args)...`, and shows just the `println()` output.

```java
System.out.println( .1 + .2 == .3);
```
Output is:
```cmd
false
```
<details><summary>Click to Show/Hide Research</summary>

[I (SWelker)](/Individuals/Scott-Welker) swerved into the issue that is the subject of this page/topic anew in the context of [Java](/Tech-Ref/Software-Development/Java). Although I've known about and battled this multiple times in the past, it had faded from memory. Here is my initial research into what, at the time, I thought was a [Java](/Tech-Ref/Software-Development/Java) issue. Actually it's a much broader issue, as you can see by reading the [Reference](#Reference) material above.

### Currency and Decimals - Problems with Float & Double

Often a degree of imprecision is not an issue. However, in some circumstances, especially financial calculations, great precision may be necessary. Enter Java's `BigDecimal`.

1. [Retain precision with double in Java](https://stackoverflow.com/a/322875/418950)
1. [...main traps of using Java's simple types double and float](https://stackoverflow.com/a/6320218/418950)
1. [Double vs. BigDecimal?](https://stackoverflow.com/a/3413493/418950)
   - > ...BigDecimal is an exact way of representing numbers. A Double has a certain precision. Working with doubles of various magnitudes (say d1=1000.0 and d2=0.001) could result in the 0.001 being dropped alltogether when summing as the difference in magnitude is so large. With BigDecimal this would not happen.
1. [How often is BigDecimal more appropriate than double in Java?](https://www.quora.com/How-often-is-BigDecimal-more-appropriate-than-double-in-Java)
   - > Problems \[with float and double\] usually stem from common misunderstanding of 1) precision, 2) exactness and 3) how floating point works, leading to a mismatch between the requirements of a program and the limitations of the type chosen. ... One has to look at the specific application to make the judgment of whether a floating point or fixed point type is appropriate, and what precision must be maintained. Sometimes this is as simple as asking, is it **simulation or accounting**?
   - > Code written with BigDecimal is harder to read and maintain. In a lot of cases, that's more important than the dozens-of-decimal-places accuracy you can get with doubles. Heck, for most non-scientific applications, floats do just fine.
1. [Why should we use BigDecimal instead of Double in the real world?](https://stackoverflow.com/a/6320316/418950)
   - > ...**loss of precision**... is very noticeable when working with either **very big numbers** or **very small numbers**. The binary representation of decimal numbers with a radix is in many cases an approximation and not an absolute value.
1. [Four common pitfalls of the BigDecimal class and how to avoid them](https://blogs.oracle.com/javamagazine/post/four-common-pitfalls-of-the-bigdecimal-class-and-how-to-avoid-them)
   - > Pitfall \#1: The **double** constructor
   - > Pitfall \#2: The static **valueOf(double)** method
   - > Pitfall \#3: The **equals(bigDecimal)** method
   - > Pitfall \#4: The **round(mathContext)** method

</details>

## JavaScript
This [JavaScript](/Tech-Ref/Software-Development/JavaScript) example uses the [Node REPL (AKA Node Shell)](/Tech-Ref/Software-Development/JavaScript/Node.js/REPL-\(Read%2DEval%2DPrint%2DLoop\)):

```cmd
C:\>node
Welcome to Node.js v14.16.0.
Type ".help" for more information.
> .1 + .2 == .3
false
```

## PowerShell
This [PowerShell](/Tech-Ref/Microsoft/PowerShell) example uses its [command-line interface (pwsh.exe)](/Tech-Ref/Microsoft/PowerShell).
- Windows PowerShell uses the [Microsoft .NET Framework](/Tech-Ref/Software-Development/NET-Framework) data types.

```cmd
C:\>pwsh.exe
PowerShell 7.2.2
Copyright (c) Microsoft Corporation.

https://aka.ms/powershell
Type 'help' to get help.

PS C:\> .1 + .2 -eq .3
False
```
:warning: These result are seemingly at odds with [PowerShell's about_Numeric_Literals](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.core/about/about_numeric_literals?view=powershell-7.2#:~:text=PowerShell%20does%20not%20support%20a,decimal%20real%20literal%20are%20significant.) where it is noted `PowerShell does not support a literal representation of a [float] value.` Here we have clearly expressed literal floating point values, as evidenced by our result, `False`, and the following example where show that PowerShell treats the literal `.1` as a `Double` (floating point) value.

```cmd
C:\>pwsh.exe
PowerShell 7.2.2
Copyright (c) Microsoft Corporation.

https://aka.ms/powershell
Type 'help' to get help.

PS C:\> .1.GetType()

IsPublic IsSerial Name                                     BaseType
-------- -------- ----                                     --------
True     True     Double                                   System.ValueType
```
   - Presumably the excerpt means only that we have no '_type suffix_' with which to force PowerShell to treat the literal as a floating point. For example, as we can do with some other data types:
      - ![image.png](/.attachments/image-39229823-2426-4450-83a9-14753124780b.png)
      - ![image.png](/.attachments/image-ae8cbaec-c8c9-46a6-892d-0c078d13c2af.png)

Notably we can use the `decimal` _type suffix_, `d`, to avoid the problem that is the subject of this page.

```cmd
C:\>pwsh.exe
PowerShell 7.2.2
Copyright (c) Microsoft Corporation.

https://aka.ms/powershell
Type 'help' to get help.

PS C:\> .1d + .2d -eq .3d
True
```

## Python
- [Python](/Tech-Ref/Software-Development/Python)

```py
>>> print(.1 + .2 == .3)
False
```

