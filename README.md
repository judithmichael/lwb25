# lwb2025

The Language Workbench (LWB) Challenge 2025 aims to understand the features different LWBs cover.
Submissions (mostly, but not exclusively, by the developers of the tools in question) implement the challenge and document it so that others can understand the implementation. Tackling a common challenge allows a better understanding of the similarities and differences between different workbenches, the design decisions underlying them, their capabilities, and their strengths and weaknesses.

This page documents the shared effort of the LWB Challenge 2025 set up by Judith Michael and Tijs van der Storm, the literature survey by Jérôme Pfeiffer, Théo Giraudet, Arnaud Blouin, Benoit Combemale, and Andreas Wortmann analyzing common features of language workbenches in literature and the implementation and documentation of all participants of the LWB Challenge 2025.

## The task: Realizing the Questionnaire Language

The following feature model describes the main features of the Questionnaire Language (QL), which should be realized using the participating Language Workbenches. 
* [Challenge Description](https://github.com/judithmichael/lwb25/blob/main/ChallengeTask.pdf)
* [QL Features Table Template](https://github.com/judithmichael/lwb25/blob/main/QLFeatures_Table_Template.xlsx)


![{974A5F0D-A117-4DDA-B522-DB805F94CB76}](https://github.com/user-attachments/assets/d9e28b78-1042-4eb9-a698-32b44a668bc7)


## The participants
(in alphabetic order)

### CINCO/CINCO Cloud 
***LWB Description***
Cinco Cloud is a holistic, cloud-native language workbench platform that has evolved from the CINCO desktop application since 2021. The platform allows the creation, distribution, and usage of graphical domain-specific languages (DSLs) and offers extensive user, project, and access management, along with the capability to deploy editors for language designers and end users. An editor enables users to design graphical DSLs, which are primarily based on graph models comprised of different node, edge, and container types. Language designers can specify languages and create models of those DSLs directly in the same environment. Syntactic and semantic changes are immediately reflected on the modeling canvas, accelerating the entire design process. Languages are specified using two textual DSLs: the Meta Graph Language (MGL) for the abstract syntax (metamodel) and static semantics, and the Meta Style Language (MSL) for the concrete syntax. Semantics and user-facing functionalities are implemented using general-purpose languages (GPLs) and an API in the editor. The API provides various implementable interfaces, such as generators, validators, hooks for user interaction, including double-click actions and CRUD operations, as well as a custom serialization logic for models. With the push of a button, language designers can distribute their languages to end users, who can then easily deploy corresponding editors directly on the web platform. The project is open source and modular. Editors and canvases can be deployed independently of the Cinco Cloud platform and integrated into other web-based projects or systems.

***Contributors***: Bernhard Steffen, Stefan Naujokat, Daniel Busch, Daniel Sami Mitwalli

***The Implementation***: https://gitlab.com/scce/cinco-cloud-language-workbench-competition-2025-questionnaire-language

### Eclipse Sirius Web
Sirius Web is a language workbench, i.e., a tool to create languages (and DSL - Domain Specific Language) as well as their modeling environments (IDE). Sirius Web is a cloud-native application with a default frontend working on a web browser. It is the successor of the Sirius Desktop project, which was a desktop application. It specializes in the development of graphical modeling languages and proposes the development of different kinds of concrete syntax (diagram, form, table, tree, deck and gantt). The development of a language is realized by using three different meta-languages for different concerns of a language: Domain DSL, to describe the abstract syntax of the language. View DSL, to describe the concrete syntax of the language. AQL (Acceleo Query Language), embedded in the View DSL, to describe the mapping between the abstract and concrete syntax. Sirius Web does not currently provide a specific language to describe the semantics, but the language designer can fall back on Java or other technologies such as Acceleo to do this. The three languages can be used directly on the Sirius Web web application, to create languages in a low-code way, or programmatically by using Sirius Web as a framework. Through the programmatic API, the language designer can directly use Ecore metamodels instead of the Domain DSL.

***Contributors***: Théo Giraudet

***The Implementation***: https://github.com/ObeoNetwork/lwc25/tree/main
  
### GEMOC 
***LWB Description***
The origins of the GEMOC Studio trace back to an initial ANR-funded research project launched in 2011, prior to the formalization of the GEMOC initiative (2013). Initially developed as a research platform to explore model execution and coordination of heterogeneous modeling languages, the Studio has since evolved through successive research collaborations and open-source contributions. Over time, it has matured into a modular workbench built on Eclipse technologies, primarily used in research and transfer contexts for designing and executing DSMLs. Today, the GEMOC Studio is hosted as an official project under the Eclipse Foundation, benefiting from a stable and open governance structure within the broader Eclipse Modeling ecosystem.
The GEMOC Studio aims to offer a comprehensive environment for designing, executing, and coordinating DSMLs, with a particular focus on executable modeling and multi-language system integration.
It integrates and assembles several major existing Eclipse technologies for language engineering, including EMF (Eclipse Modeling Framework) for metamodeling and model management, Sirius Desktop for the definition of graphical editors, and Xtext for the specification of textual editors.

***Contributors***: Didier Vojtisek, Benoit Combemale

***The Implementation***: https://github.com/gemoc/ql-gemoc-lwb2025
  
### Gentleman
***LWB Description***
Gentleman is a lightweight web‑based projectional editor that aims to make modeling more accessible to domain experts and practitioners (outside traditional software engineering). The editor surface is a composition of projections (graphical, tabular, textual, and interactive widgets) bound to concepts that structure the model data. Gentleman directly edits the Abstract syntax tree (AST) through projections. It supports a wide range of notations—textual, graphical, tabular, and interactive widgets. Gentleman emphasizes simplicity and flexibility. Its minimalistic web-based design reduces visual clutter and focuses attention on the modeling activity itself. By being distributed as a JavaScript library, it can be embedded in any web application, enabling smooth integration into existing workflows. Projections can be styled, customized, and reused, making the tool adaptable to various domains and user needs.

***Contributors***: Eugene Syriani, Louis-Edouard Lafontant

***The Implementation***: https://github.com/geodes-sms/gentleman-lwb25

### Jetbrains MPS 
JetBrains MPS is an open‐source language workbench designed for creating and using domain-specific languages (DSLs) through a unique projectional editing approach. Instead of relying on traditional text parsing, MPS stores code directly as an abstract syntax tree (AST), allowing developers to mix textual, graphical, and tabular notations seamlessly. This method eliminates grammatical ambiguities and supports the flexible composition and reuse of language components. Key features include the ability to define custom languages by setting up abstract syntax, editor projections, type systems, and constraints. MPS enables direct manipulation of the AST with multiple notations and provides built-in code generation, which translates high-level DSL code into lower-level executable code in languages like Java or C. The integrated development environment mirrors modern IDE functionalities such as code completion, refactoring, and debugging, making it a comprehensive tool for language-oriented programming. Originating from early 2000s research at JetBrains and inspired by the Language-Oriented Programming paradigm, MPS evolved from an experimental prototype into a production-ready platform. Public beta versions appeared around 2007–2008, with a stable version launched in 2009 under an open-source license. Its maturity has fostered adoption in diverse fields—ranging from embedded systems and enterprise applications to complex business logic and academic research—demonstrating its practical impact on both industry and education. Overall, JetBrains MPS has redefined software development by empowering developers and domain experts to tailor languages specifically to their problems, thereby enhancing productivity and precision in crafting complex systems.

***Contributors***: Klemens Schindler, Eugen Schindler

***The Implementation***: https://github.com/DSLFoundry/mps-lwc25
  
### jjodel 
***LWB Description***

***Contributors***:

***The Implementation***:
  
### Langium 
***LWB Description***

***Contributors***:

***The Implementation***:
  
### MetaEdit+
***LWB Description***

***Contributors***:

***The Implementation***:
  
### MontiCore 
MontiCore is a language workbench for the efficient engineering and provision of textual software languages. In MontiCore, languages are realized based on context-free grammars (CFGs) in EBNF. This enables language engineers to define concrete and abstract syntax simultaneously. Based on the production rules defined within a CFG, MontiCore generates the required infrastructure for model (or program) processing. The derived processing software is based on the Java programming language. It comprises basic components such as a parser, abstract syntax classes, as well as infrastructure for context conditions (CoCos), visitors, and symbol management. A core feature of MontiCore is the compositional software language engineering (SLE). It supports seamlessly integrating various language modules or even fully-fletched languages via different composition techniques: Inheritance, conservative extension, language embedding (or unification), aggregation. These integration techniques include composing the holistic generated infrastructure of the languages as well as handwritten extensions. The parser, abstract syntax, CoCos and Somboltable are designed for composability and black-box reusability. Generally, MontiCore generatively supports various design patterns that are specifically tailored with language composition in mind. Additionally, MontiCore provides an extensive library of reusable language components. These enable developers to combine different variants of, for instance, expressions, statements, literals, or types and embed these in their own language.

***Contributors***: Bernhard Rumpe, Alex Lüpges, Nico Jansen 

***The Implementation***: https://github.com/MontiCore/lwb-competition
  
### Neverlang
Neverlang was born in 2009 as a framework for the creation of sectional compilers. The original implementation leveraged AspectJ to implement the _syntax-directed translation_ technique by weaving the semantics with the respective syntactic AST nodes. A novel version was developed in 2012; it integrated the Dynamically EXTEnsible Recognizer (**DEXTER**) with a revised and bootstrapped Neverlang compiler. Since then, the Neverlang compiler was evolved to include several new features, such as (i) polyglot semantic actions for all JVM-based languages, as well as for others, provided that a translator is internally defined, (ii) integrated _Language Product Line_ (LPL) support, (iii) _Language Server Protocol_ (LSP) and _Debug Adapter Protocol_ (DAP), (iv) and new syntactic constructs to support smoother and more _fine-grained_ language composition.
Another peculiar aspect of Neverlang is the ability to update the syntax and semantics of a language at runtime, exploiting the _dynamic software updating_ technique. Neverlang was at the basis of several international scientific publications and was used in industrial settings. It provides _editing support_ for the languages developed with it using LSP, providing language-specific services, such as semantic highlighting, code completion, and error checking, while the DAP is used to provide debugging capabilities, such as breakpoints, stepping, and variable inspection. Furthermore, the Neverlang ecosystem provides a _plugin generator_ for widely used editors, such as _Visual Studio Code_.

***Contributors***: Walter Cazzola, Federico Bruzzone, Luca Favalli

***The Implementation***: https://github.com/AdaptLab-CS/neverlang-questionnaire-language
  
### Rascal
***LWB Description***

***Contributors***: Tijs van der Storm

***The Implementation***: https://github.com/cwi-swat/tiny-ql
  
### Spoofax 
***LWB Description***

***Contributors***:

***The Implementation***:
  
### TextX
***LWB Description***
textX (since 2014, https://github.com/textX/) is a Python meta-language — a language for defining domain-specific languages (DSLs). From a single grammar definition, textX automatically generates a meta-model (represented as Python
classes) and a corresponding parser. This parser processes expressions written in the defined DSL and constructs a graph of Python objects (the model) that conforms to the meta-model. Initially inspired by Eclipse Xtext, textX was conceived as a lightweight Python alternative. However, it has since evolved with distinct differences. textX follows a modular architecture, enabling languages and generators to be developed as independent Python projects.
Additional tooling — such as Language Server Protocol (LSP) support, syntax highlighting, project scaffolding, and template-engine integration — is provided by separate projects under the textX organization.

***Contributors***: Igor Dejanovic

***The Implementation***: https://github.com/igordejanovic/lwc2025
  
## Features of language workbenches

We use a feature model capturing their major features to compare the different language workbenches better.
This feature model captures the design space of language workbenches as analyzed in the literature by Jérôme Pfeiffer, Théo Giraudet, Arnaud Blouin, Benoit Combemale, and Andreas Wortmann. 

* [Language Workbench Feature Diagram](https://github.com/judithmichael/lwb25/blob/main/LanguageWorkbench_FeatureDiagram.png)
* [Language Workbench Description](https://github.com/judithmichael/lwb25/blob/main/LanguageWorkbench_Description.png)
* [Modeling Workbench Feature Diagram](https://github.com/judithmichael/lwb25/blob/main/ModelingWorkbench_FeatureDiagram.png)
* [Modeling Workbench Description](https://github.com/judithmichael/lwb25/blob/main/ModelingWorkbench_Description.png)



An older version can be found [here](https://doi.org/10.1016/j.cl.2015.08.007).



