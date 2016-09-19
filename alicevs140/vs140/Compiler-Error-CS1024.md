---
title: "Compiler Error CS1024"
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
ms.assetid: 41f587cb-1958-4eb6-9f8d-c03500e55e21
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1024
Preprocessor directive expected  
  
 A line began with the pound symbol (#), but the subsequent string was not a valid [preprocessor directive](../vs140/C#-Preprocessor-Directives.md).  
  
 The following sample generates CS1024:  
  
```  
// CS1024.cs  
#import System   // CS1024  
```