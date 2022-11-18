[Home](/Slalom-LLC/Slalom-Consulting) | [Glossary](/Glossary) | [Tech Ref](/Tech-Ref) | [Software Development](/Tech-Ref/Software-Development) | [Java](/Tech-Ref/Software-Development/Java)

[[_TOC_]]

---
# Introduction
This page reflects [my (SWelker)](/Individuals/Scott-Welker) collected and curated [Java](/Tech-Ref/Software-Development/Java) development guidance.

## Reference
1. [Oracle: Code Conventions for the Java TM Programming Language](https://www.oracle.com/java/technologies/javase/codeconventions-contents.html)
   - [Oracle: 9 - Naming Conventions](https://www.oracle.com/java/technologies/javase/codeconventions-namingconventions.html)
1. [Developer.com: Top 10 Java Coding Standards](https://www.developer.com/design/top-10-java-coding-guidelines/)

---
# Topics
1. [Java](/Tech-Ref/Software-Development/Java).
1. [Programming 'Case' Types](/Tech-Ref/Software-Development/Programming-Case-Types).

---
# Conventions and Guidelines

## Identifiers are case sensitive and must be compiler legal.
- See [Naming Conventions](#naming-conventions).
- Cannot be a [Java](/Tech-Ref/Software-Development/Java) reserved word (keyword).
- Composed of only Unicode characters, numbers, currency symbols, and connecting characters (`_` underscore).
- Must start with a letter, a currency character (`$`), or a connecting character (`_` underscore).

## Conventions apply to Class, Method, and Variable Names
- See [Naming Conventions](#naming-conventions).

## Naming Conventions
- [Wikipedia: Naming converntion](https://en.wikipedia.org/wiki/Naming_convention_(programming))
- [Java](/Tech-Ref/Software-Development/Java) naming conventions are a set of rules to make Java code look uniform across Java projects and the library. They are not strict rules, but a guideline to adhere to as a good programming practice.
- [Programming 'Case' Types](/Tech-Ref/Software-Development/Programming-Case-Types).

### Class, Enum, Interface, and Annotation Names in PascalCase
- Class, enum, interface, and annotation names are typed in [PascalCase](/Tech-Ref/Software-Development/Programming-Case-Types#pascalcase) but tend to be single words. Therefore they are typically things like `Thread`, `Runnable`, or `@Override`.
- Class names are typically nouns, e.g. `Car` or `User`.
   - Try to keep your class names simple and descriptive. Use whole words-avoid acronyms and abbreviations (unless the abbreviation is much more widely used than the long form, such as URL or HTML).
- Interface names are typically adjectives, e.g. `Runnable` or `Serializable`.

### Constant Names in MACRO_CASE
- Constant names are typed in [MACRO_CASE](/Tech-Ref/Software-Development/Programming-Case-Types#macrocase).

### Local Variables in camelCase
- Local variables are typed in [camelCase](/Tech-Ref/Software-Development/Programming-Case-Types#camelcase).
- Variable names should be short yet meaningful. The choice of a variable name should be mnemonic- that is, designed to indicate to the casual observer the intent of its use. **One-character variable names should be avoided** except for temporary "throwaway" variables. Common names for temporary variables are `i`, `j`, `k`, `m`, and `n` for integers; `c`, `d`, and `e` for characters.
 
### Methods and Field Names in camelCase
- Methods and field names are typed in a [camelCase](/Tech-Ref/Software-Development/Programming-Case-Types#camelcase).
- Method names should be verbs.

### Package Names in Lowercase
- [Package](/Tech-Ref/Software-Development/Java/Java-Language/Package-\(Java\)) names are types in lowercase: `javax.sql`, `org.junit`, `java.lang`.
- The prefix of a unique package name should be one of the top-level domain names, currently `com`, `edu`, `gov`, `mil`, `net`, `org`, or one of the English two-letter codes identifying countries as specified in [ISO Standard 3166](https://en.wikipedia.org/wiki/List_of_ISO_3166_country_codes#Current_ISO_3166_country_codes), 1981.
   - Subsequent components of the package name vary according to an organization's own internal naming conventions. Such conventions might specify that certain directory name components be division, department, project, machine, or login names.