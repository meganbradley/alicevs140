---
title: "Compiler Warning (level 1) CS3013"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 00b3bbe1-f2a0-465c-be0e-1af700c5753d
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) CS3013
Added modules must be marked with the CLSCompliant attribute to match the assembly  
  
 A module that was compiled with the [/target:module](../vs140/-target-module--C#-Compiler-Options-.md) compiler option was added to a compilation with [/addmodule](../Topic/-addmodule%20\(C%23%20Compiler%20Options\).md). However, the module's compliance with the Common Language Specification (CLS) does not agree with the CLS state of the current compilation.  
  
 CLS compliance is indicated with the module attribute. For example, `[module:CLSCompliant(true)]` indicates that the module is CLS compliant, and `[module:CLSCompliant(false)]` indicates that the module is not CLS compliant. The default is `[module:CLSCompliant(false)]`. For more information on the CLS, see [What Is the Common Language Specification](assetId:///4f0b77d0-4844-464f-af73-6e06bedeafc6).