[Home](/Slalom-LLC/Slalom-Consulting) | [Glossary](/Glossary) | [Tech Ref](/Tech-Ref) | [Software Development](/Tech-Ref/Software-Development) | [Java](/Tech-Ref/Software-Development/Java)

[[_TOC_]]

---
# Introduction
|:seedling: [Wiki Gardening](/Tech-Ref/Wiki/Wiki-Gardening)|
|:-|
| Some JDK information is recorded here, [Tips and Tricks, Windows, Java Development Kit (JDK) with JRE](/Tech-Ref/Software-Development/Java#java-development-kit-(jdk)-with-jre). |

"_***Java Development Kit (JDK)*** is an implementation of either one of the [Standard Edition](https://en.wikipedia.org/wiki/Java_Platform,_Standard_Edition), [Enterprise Edition](https://en.wikipedia.org/wiki/Java_Platform,_Enterprise_Edition), or [Micro Edition](https://en.wikipedia.org/wiki/Java_Platform,_Micro_Edition) platforms released by [Oracle Corporation](/Tech-Ref/Oracle-Corporation) in the form of a binary product aimed at [Java](/Tech-Ref/Software-Development/Java) developers on [Solaris](/Tech-Ref/Unix), [Linux](/Tech-Ref/Linux), [macOS](/Tech-Ref/Apple-Inc/Mac-\(Macintosh\)/macOS) or [Windows](/Tech-Ref/Microsoft/Windows). The JDK includes a private JVM and a few other resources to finish the development of a [Java](/Tech-Ref/Software-Development/Java) application._"

- :bulb: ***JDK*** 8 is a superset of [JRE](/Tech-Ref/Software-Development/Java/JRE-\(Java-Runtime-Environment\)) 8, and contains everything that is in [JRE](/Tech-Ref/Software-Development/Java/JRE-\(Java-Runtime-Environment\)) 8, plus tools such as the compilers and debuggers necessary for developing applets and applications. [JRE](/Tech-Ref/Software-Development/Java/JRE-\(Java-Runtime-Environment\)) 8 provides the libraries, the [Java Virtual Machine (JVM)](/Tech-Ref/Software-Development/Java/JRE-\(Java-Runtime-Environment\)), and other components to run [applets](/Tech-Ref/Software-Development/Java/Java-Applet) and applications written in the [Java programming language](/Tech-Ref/Software-Development/Java/Java-Language). Note that the [JRE](/Tech-Ref/Software-Development/Java/JRE-\(Java-Runtime-Environment\)) includes components not required by the [Java SE](/Tech-Ref/Software-Development/Java/Java-Platform-Editions/Java-SE-\(Standard-Edition\)) specification, including both standard and non-standard [Java](/Tech-Ref/Software-Development/Java) components.

## Reference
1. [Wikipedia: Java Development Kit](https://en.wikipedia.org/wiki/Java_Development_Kit)
1. [The JDKs: Which One to Use?](https://dzone.com/articles/java-and-the-jdks-which-one-to-use)

---
# Topics
1. [Java](/Tech-Ref/Software-Development/Java).
1. [JDK Mission Control (JMC)](/Tech-Ref/Software-Development/Java/JRE-\(Java-Runtime-Environment\)/JVM-\(Java-Virtual-Machine\)/JMC-\(JDK-Mission-Control\)).
1. [Linux](/Tech-Ref/Linux).
1. [macOS](/Tech-Ref/Apple-Inc/Mac-\(Macintosh\)/macOS).
1. [Oracle](/Tech-Ref/Oracle-Corporation).
1. [Unix](/Tech-Ref/Unix).
1. [Windows](/Tech-Ref/Microsoft/Microsoft-Windows).

---
# Java Development Kits
Here are some of the more noteworthy JDKs. Credit to: [DZone: The JDKs: Which One to Use?](https://dzone.com/articles/java-and-the-jdks-which-one-to-use)

## Oracle JDK (commercial)
- :moneybag: This is the main distributor of [Java](/Tech-Ref/Software-Development/Java) 11 (already released). This is a commercial version of the brand with paid support. It can be downloaded and used free of charge for development use only. It cannot be used in production without paying [Oracle](/Tech-Ref/Oracle-Corporation) (so it's a trap for the unsuspecting). [Oracle](/Tech-Ref/Oracle-Corporation) intends to provide full, paid support until 2026 or later. Note that, unlike the past, [Oracle](/Tech-Ref/Oracle-Corporation) JDK is not "better" than the [OpenJDK](/Tech-Ref/Software-Development/Java/OpenJDK-\(Open-Java-Development-Kit\)) build (as long as both are at the same level as the security patch).

## OpenJDK Build by Oracle (free)
See also [OpenJDK](/Tech-Ref/Software-Development/Java/OpenJDK-\(Open-Java-Development-Kit\)).
- :free: These are free and unbranded versions of the [OpenJDK](/Tech-Ref/Software-Development/Java/OpenJDK-\(Open-Java-Development-Kit\)) under the [GPL license with Classpath Exception (secure for business use)](/Tech-Ref/Software-Development/Java/GNU-Classpath-Exception). These builds are only available in the first six months of a release. For [Java](/Tech-Ref/Software-Development/Java) 11, the expectation is that there will be [Java](/Tech-Ref/Software-Development/Java) 11.0.0 and then two security patches, 11.0.1 and 11.0.2. To continue using the [OpenJDK](/Tech-Ref/Software-Development/Java/OpenJDK-\(Open-Java-Development-Kit\)) build by [Oracle](/Tech-Ref/Oracle-Corporation) with security patches, you would have to switch to [Java](/Tech-Ref/Software-Development/Java) 12 within a month after the launch. Note that the provision of security patches is not the same as support. Support involves paying someone to do the sorting and acting on the error reports.

## AdoptOpenJDK Build (free)
- :free: These are free and unbranded [OpenJDK](/Tech-Ref/Software-Development/Java/OpenJDK-\(Open-Java-Development-Kit\)) builds under the [GPL license with the Classpath Exception](/Tech-Ref/Software-Development/Java/GNU-Classpath-Exception). Unlike [Oracle's](/Tech-Ref/Oracle-Corporation) [OpenJDK](/Tech-Ref/Software-Development/Java/OpenJDK-\(Open-Java-Development-Kit\)) builds, these builds will continue for a much longer period for major versions such as [Java](/Tech-Ref/Software-Development/Java) 11. The versions of [Java](/Tech-Ref/Software-Development/Java) 11 will continue for four years, one year after the next major release. AdoptOpenJDK is a community group. They will provide builds as long as other groups create and publish security fixes to a source repository in [OpenJDK](/Tech-Ref/Software-Development/Java/OpenJDK-\(Open-Java-Development-Kit\)). Both IBM and Red Hat have indicated that they intend to provide these security patches.

## AdoptOpenJDK OpenJ9 Build (free)
- :free: In addition to standard [OpenJDK](/Tech-Ref/Software-Development/Java/OpenJDK-\(Open-Java-Development-Kit\)) builds, AdoptOpenJDK will also provide builds with OpenJ9 instead of HotSpot. OpenJ9 was originally the IBM JVM, but OpenJ9 is now open source in Eclipse. This one, in fact, is something to be studied.

## Red Hat OpenJDK Build (commercial)
- :moneybag: Red Hat provides [OpenJDK](/Tech-Ref/Software-Development/Java/OpenJDK-\(Open-Java-Development-Kit\)) builds through Red Hat Enterprise Linux (RHEL), which is a commercial product with paid support. They are very good at providing security fixes back to [OpenJDK](/Tech-Ref/Software-Development/Java/OpenJDK-\(Open-Java-Development-Kit\)). In the past, Red Hat has run the [Java](/Tech-Ref/Software-Development/Java) 6 and 7 security update project. The Red Hat build is better integrated with the operating system, so it is not a pure [OpenJDK](/Tech-Ref/Software-Development/Java/OpenJDK-\(Open-Java-Development-Kit\)) build (no end-user JDK)

## Azul Zulu (commercial)
- :moneybag: Zulu is a branded version of [OpenJDK](/Tech-Ref/Software-Development/Java/OpenJDK-\(Open-Java-Development-Kit\)) with paid commercial support. In addition, Azul provides some Zulu constructions for free as part of the "Zulu Community;" however, there are no specific commitments regarding the availability of these free constructions. Azul has an extensive plan to commercially support Zulu, including plans to support [Java](/Tech-Ref/Software-Development/Java) 9, 13, and 15, unlike any other vendor.

## Amazon Corretto (free)
- :free: Among all, it is the newest option. Corretto is a no-cost build of [OpenJDK](/Tech-Ref/Software-Development/Java/OpenJDK-\(Open-Java-Development-Kit\)) with long-term support passing through the TCK. It is under the standard [GPL + CE license](/Tech-Ref/Software-Development/Java/GNU-Classpath-Exception) of all versions of [OpenJDK](/Tech-Ref/Software-Development/Java/OpenJDK-\(Open-Java-Development-Kit\)). Amazon will add its own patches and run Corretto on [AWS](/Tech-Ref/AWS-\(Amazon-Web-Services\)), so it will be heavily used (it has already been placed on some products). Support for [Java](/Tech-Ref/Software-Development/Java) 8 will be at least until June 2023.

## Others (commercial and free)
- There are other implementations of JDK, such as IBM and SAPMachine. However, these builds are not yet as used as the others, so I decided to leave their out of this short article.

# Components (Typical)

## Java Archive Tool 
- [Java Archive Tool](/Tech-Ref/Software-Development/Java/JAR-\(Java-ARchive\)#jar.exe).

---
# Tips and Tricks

## Getting Started

### Windows 10 (08/201)

#### Java Development Kit (JDK) with JRE
- See [Java, Tips and Tricks, Java Development Kit (JDK) with JRE](/Tech-Ref/Software-Development/Java#java-development-kit-(jdk)-with-jre).
