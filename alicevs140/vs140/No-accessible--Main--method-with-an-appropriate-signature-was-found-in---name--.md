---
title: "No accessible &#39;Main&#39; method with an appropriate signature was found in &#39;&lt;name&gt;&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-visual-basic
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3f40bacd-3fac-4741-b204-852f693d4340
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# No accessible &#39;Main&#39; method with an appropriate signature was found in &#39;&lt;name&gt;&#39;
Command-line applications must have a `Sub Main` defined. `Main` must be declared as `Public Shared` if it is defined in a class, or as `Public` if defined in a module.  
  
 For more information on `Main`, see [NIB: Visual Basic Version of Hello, World](assetId:///9d030b60-e148-4366-a462-69532f02294c).  
  
 **Error ID:** BC30737  
  
### To correct this error  
  
-   Define a `Public Sub Main` procedure for your project. Declare it as `Shared` if and only if you define it inside a class.  
  
## See Also  
 [NIB: Visual Basic Version of Hello, World](assetId:///9d030b60-e148-4366-a462-69532f02294c)   
 [Structure of a Visual Basic Program](../vs140/Structure-of-a-Visual-Basic-Program.md)   
 [Procedures in Visual Basic](../vs140/Procedures-in-Visual-Basic.md)