[Home](/Slalom-LLC/Slalom-Consulting) | [Glossary](/Glossary) | [Tech Ref](/Tech-Ref) | [Software Development](/Tech-Ref/Software-Development) | [Java](/Tech-Ref/Software-Development/Java) | [Java Foundation Classes (JFC)](/Tech-Ref/Software-Development/Java/Java-Platform-Editions/Java-SE-\(Standard-Edition\)/JFC-\(Java-Foundation-Classes\))
**Disambiguation:** [AWT](/Tech-Ref/Software-Development/Java/Java-Platform-Editions/Java-SE-\(Standard-Edition\)/JFC-\(Java-Foundation-Classes\)/AWT-\(Abstract-Window-Toolkit\)), [Standard Widget Toolkit](/Tech-Ref/Software-Development/Java/Standard-Widget-Toolkit).

[[_TOC_]]

---
# Introduction
***Swing Model Architecture*** refers to the [Swing Widget Toolkit's](/Tech-Ref/Software-Development/Java/Java-Platform-Editions/Java-SE-\(Standard-Edition\)/JFC-\(Java-Foundation-Classes\)/Swing) <mark>modified</mark> [Model View Controller](/Tech-Ref/Software-Development/Software-Design-Pattern/MVC-\(Model-View-Controller\)) design._"

"_The traditional [MVC pattern](/Tech-Ref/Software-Development/Software-Design-Pattern/MVC-\(Model-View-Controller\)) divides an application into three parts: a model, a view and a controller. The **model** represents the data in the application. The **view** is the visual representation of the data. And finally the **controller** processes and responds to events, typically user actions, and may invoke changes on the model. The idea is to separate the data access and business logic from data presentation and user interaction, by introducing an intermediate component: the controller._"

"_The [Swing toolkit](/Tech-Ref/Software-Development/Java/Java-Platform-Editions/Java-SE-\(Standard-Edition\)/JFC-\(Java-Foundation-Classes\)/Swing) uses a modified [MVC design pattern](/Tech-Ref/Software-Development/Software-Design-Pattern/MVC-\(Model-View-Controller\)). It has a **single UI object for both the view and the controller**. This modified [MVC](/Tech-Ref/Software-Development/Software-Design-Pattern/MVC-\(Model-View-Controller\)) is sometimes called a separable model architecture._"

"_In the [Swing toolkit](/Tech-Ref/Software-Development/Java/Java-Platform-Editions/Java-SE-\(Standard-Edition\)/JFC-\(Java-Foundation-Classes\)/Swing), every component has its model, even the basic ones like buttons. There are two kinds of models in [Swing toolkit](/Tech-Ref/Software-Development/Java/Java-Platform-Editions/Java-SE-\(Standard-Edition\)/JFC-\(Java-Foundation-Classes\)/Swing):_"

   - "_state models_"
   - "_data models_"

"_The state models handle the state of the component. For example the model keeps track whether the component is selected or pressed. The data models handle data they work with._"

## Reference
1. [ZetCode: Java Swing Model Architecture](https://zetcode.com/javaswing/swingmodels/)
1. [Wikipedia: Swing, Architecture](https://en.wikipedia.org/wiki/Swing_(Java)#Architecture)

---
# Topics
1. [Java](/Tech-Ref/Software-Development/Java).
1. [Java Foundation Classes (JFC)](/Tech-Ref/Software-Development/Java/Java-Platform-Editions/Java-SE-\(Standard-Edition\)/JFC-\(Java-Foundation-Classes\)):
   - [Swing](/Tech-Ref/Software-Development/Java/Java-Platform-Editions/Java-SE-\(Standard-Edition\)/JFC-\(Java-Foundation-Classes\)/Swing).
