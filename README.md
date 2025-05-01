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
* LWB Description:
* Contributors:
* The Implementation

### Eclipse Sirius Web
* ***LWB Description***: Sirius Web is a language workbench, i.e., a tool to create languages (and DSL - Domain Specific Language) as well as their modeling environments (IDE). Sirius Web is a cloud-native application with a default frontend working on a web browser. It is the successor of the Sirius Desktop project, which was a desktop application. It specializes in the development of graphical modeling languages and proposes the development of different kinds of concrete syntax (diagram, form, table, tree, deck and gantt). The development of a language is realized by using three different meta-languages for different concerns of a language: Domain DSL, to describe the abstract syntax of the language. View DSL, to describe the concrete syntax of the language. AQL (Acceleo Query Language), embedded in the View DSL, to describe the mapping between the abstract and concrete syntax. Sirius Web does not currently provide a specific language to describe the semantics, but the language designer can fall back on Java or other technologies such as Acceleo to do this. The three languages can be used directly on the Sirius Web web application, to create languages in a low-code way, or programmatically by using Sirius Web as a framework. Through the programmatic API, the language designer can directly use Ecore metamodels instead of the Domain DSL.
* ***Contributors***: Théo Giraudet
* ***The Implementation***: https://github.com/ObeoNetwork/lwc25/tree/main
  
### GEMOC 
* ***LWB Description***:
* ***Contributors***:
* ***The Implementation***:
  
### Gentleman
* ***LWB Description***:
* ***Contributors***:
* ***The Implementation***:
  
### jjodel 
* ***LWB Description***:
* ***Contributors***:
* ***The Implementation***:
  
### Langium 
* ***LWB Description***:
* ***Contributors***:
* ***The Implementation***:
  
### MetaEdit+
* ***LWB Description***:
* ***Contributors***:
* ***The Implementation***:
  
### MontiCore 
* ***LWB Description***:
* ***Contributors***:
* ***The Implementation***:
  
### MPS 
* ***LWB Description***:
* ***Contributors***:
* ***The Implementation***:
  
### Neverlang
* ***LWB Description***:
* ***Contributors***:
* ***The Implementation***:
  
### Rascal
* ***LWB Description***:
* ***Contributors***:
* ***The Implementation***:
  
### Spoofax 
* ***LWB Description***:
* ***Contributors***:
* ***The Implementation***:
  
### TextX
* ***LWB Description***:
* ***Contributors***:
* ***The Implementation***:
  
## Features of language workbenches

We use a feature model capturing their major features to compare the different language workbenches better.
This feature model captures the design space of language workbenches as analyzed in the literature by Jérôme Pfeiffer, Théo Giraudet, Arnaud Blouin, Benoit Combemale, and Andreas Wortmann. 

* [Language Workbench Feature Diagram](https://github.com/judithmichael/lwb25/blob/main/LanguageWorkbench_FeatureDiagram.png)
* [Language Workbench Description](https://github.com/judithmichael/lwb25/blob/main/LanguageWorkbench_Description.png)
* [Modeling Workbench Feature Diagram](https://github.com/judithmichael/lwb25/blob/main/ModelingWorkbench_FeatureDiagram.png)
* [Modeling Workbench Description](https://github.com/judithmichael/lwb25/blob/main/ModelingWorkbench_Description.png)



An older version can be found [here](https://doi.org/10.1016/j.cl.2015.08.007).



