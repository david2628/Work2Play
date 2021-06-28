# Software Architecture Document

# Table of Contents
- [Introduction](#1-introduction)
    - [Purpose](#11-purpose)
    - [Scope](#12-scope)
    - [Definitions, Acronyms and Abbreviations](#13-definitions-acronyms-and-abbreviations)
    - [References](#14-references)
    - [Overview](#15-overview)
- [Architectural Representation](#2-architectural-representation)
- [Architectural Goals and Constraints](#3-architectural-goals-and-constraints)
- [Use-Case View](#4-use-case-view)
    - [Use-Case Realizations](#41-use-case-realizations)
- [Logical View](#5-logical-view)
    - [Overview](#51-overview)
    - [Architecturally Significant Design Packages](#52-architecturally-significant-design-packages)
    - [Pattern](#53-Pattern)
- [Process View](#6-process-view)
- [Deployment View](#7-deployment-view)
- [Implementation View](#8-implementation-view)
    - [Overview](#81-overview)
    - [Layers](#82-layers)
- [Data View](#9-data-view)
- [Size and Performance](#10-size-and-performance)
- [Quality](#11-quality)

## 1. Introduction
### 1.1 Purpose
This document provides a quick architectural overview of the system. It is intended to capture the significant architectural decisions which have been made on the system.

### 1.2 Scope
This document describes the architecture of the Work2Play Project.

### 1.3 Definitions, Acronyms and Abbreviations
|			Abbreviation									                |	Explanation		|
|---------------------------------------------------|---------------|
| *** | *** |

### 1.4 References
n/a
### 1.5 Overview
The architectural details will be described in the following sections. This includes the class diagrams which gives an overview about the whole project.

## 2. Architectural Representation
We are developing a App that is designed for Android so a normal MVC representation is good.
The data is safed in a local SQLite Database. Some variables are stored in the Shared Preferences.

![mvc]

## 3. Architectural Goals and Constraints
TBD.

## 4. Use-Case View
### 4.1 Use-Case Realizations

![oucd2]
## 5. Logical View
### 5.1 Overview
n/a
### 5.2 Architecturally Significant Design Packages
The class diagram; containing all Data Access Objects, Models and Controllers that we will need to finish for the basic functionality:

![Class Diagram]

### 5.3 Pattern
TBD
## 7. Deployment View
n/a
## 8. Implementation View
### 8.1 Overview
n/a
### 8.2 Layers
n/a
## 9. Data View
This is a representation of our SQLite database in a ER-Model. It displays the implementation of the model and shows relations between the objects.

![databasemodel]

## 10. Size and Performance
n/a
## 11. Quality
n/a


[mvc]: ./PNGs/Arcitechture-Diagramm.png "Model-View-Viewmodel"

[oucd2]: ./PNGs/UCD.png "Overall Use Case Diagram Semester 2"

[Class Diagram]: ./PNGs/ClassDiagramm.png "Class Diagram"

[databasemodel]: ./PNGs/database-model.png "ER-Modell"
