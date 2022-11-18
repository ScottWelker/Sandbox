[Home](/Slalom-LLC/Slalom-Consulting) | [Glossary](/Glossary) | [Tech Ref](/Tech-Ref) | [Software Development](/Tech-Ref/Software-Development) | [DevOps](/Tech-Ref/Software-Development/DevOps-\(Development-and-IT-Operations\)) | [Modeling](/Tech-Ref/Software-Development/Modeling)

[[_TOC_]]

---
# Introduction
"_***PlantUML*** is an open-source tool allowing users to create diagrams from a plain text language. Besides various [UML](/Tech-Ref/Software-Development/Modeling/UML-\(Unified-Modeling-Language\)) diagrams, PlantUML has support for various other software development related formats (such as Archimate, Block diagram, BPMN, C4, Computer network diagram, ERD, Gantt chart, Mind map, and WBD), as well as visualization of [JSON](/Tech-Ref/Software-Development/JSON-\(JavaScript-Object-Notation\)) and [YAML](/Tech-Ref/Software-Development/YAML-\(YAML-Ain't-Markup-Language\)) files._"

"_The language of PlantUML is an example of a domain-specific language. Besides its own DSL, PlantUML also understands AsciiMath, Creole, DOT, and LaTeX. It uses Graphviz software to layout its diagrams and Tikz for LaTeX support. Images can be output as PNG, SVG, LaTeX and even ASCII art._"

## Reference
1. [Wikipedia: PlantUML](https://en.wikipedia.org/wiki/PlantUML)

## Notes
1. :warning: [SWelker](/Individuals/Scott-Welker): The on-line, web version passes your diagrams as plain text. This makes it **insecure**. 
1. :+1: Recommend the [Docker](/Tech-Ref/Software-Development/DevOps-\(Development-and-IT-Operations\)/Docker) ***PlantUML Server*** image for local, secure use:
      - https://hub.docker.com/r/plantuml/plantuml-server
      - You can run Plantuml with tomcat or jetty container:
         - :+1:`docker run -d -p 8080:8080 plantuml/plantuml-server:tomcat`
            - The server is now listing to `http://localhost:8080`.
         - :disappointed: `docker run -d -p 8080:8080 plantuml/plantuml-server:jetty`
1. **Updates:** 
   - [Stop Docker](/Tech-Ref/Software-Development/DevOps-\(Development-and-IT-Operations\)/Docker#stop-docker).
   - **[Docker Pull](/Tech-Ref/Software-Development/DevOps-\(Development-and-IT-Operations\)/Docker#pull-(update)):** `docker pull plantuml/plantuml-server`

---
# Topics
1. [Docker](/Tech-Ref/Software-Development/DevOps-\(Development-and-IT-Operations\)/Docker).
1. [Modeling](/Tech-Ref/Software-Development/Modeling).
1. [Unified Modeling Language (UML)](/Tech-Ref/Software-Development/Modeling/UML-\(Unified-Modeling-Language\)).
