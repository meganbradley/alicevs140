---
title: "Creating Registrar Scripts"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: cbd5024b-8061-4a71-be65-7fee90374a35
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Creating Registrar Scripts
A registrar script provides data-driven, rather than API-driven, access to the system registry. Data-driven access is typically more efficient since it takes only one or two lines in a script to add a key to the registry.  
  
 The [ATL Control Wizard](../vs140/ATL-Control-Wizard.md) automatically generates a registrar script for your COM server. You can find this script in the .rgs file associated with your object.  
  
 The ATL Registrar's Script Engine processes your registrar script at run time. ATL automatically invokes the Script Engine during server setup.  
  
 This article covers the following topics related to the registrar scripts:  
  
-   [Understanding Backus Nauer Form (BNF) Syntax](../vs140/Understanding-Backus-Nauer-Form--BNF--Syntax.md)  
  
-   [Understanding Parse Trees](../vs140/Understanding-Parse-Trees.md)  
  
-   [Registry Scripting Examples](../vs140/Registry-Scripting-Examples.md)  
  
-   [Using Replaceable Parameters (The Registrar's Preprocessor)](../vs140/Using-Replaceable-Parameters--The-Registrar-s-Preprocessor-.md)  
  
-   [Invoking Scripts](../vs140/Invoking-Scripts.md)  
  
## See Also  
 [Registry Component (Registrar)](../vs140/ATL-Registry-Component--Registrar-.md)