---
title: "Ordinal is not valid"
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
ms.assetid: 7459562b-cd4f-4590-95e0-6126ae3589a5
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Ordinal is not valid
Your call to a dynamic-link library (DLL) indicated to use a number instead of a procedure name, using the `#num` syntax. This error has the following possible causes:  
  
-   An attempt to convert the `#num` expression to an ordinal failed.  
  
-   The `#num` specified does not specify any function in the DLL.  
  
-   A type library has an invalid declaration resulting in internal use of an invalid ordinal number.  
  
### To correct this error  
  
1.  Make sure the expression represents a valid number, or call the procedure by name.  
  
2.  Make sure `#num` identifies a valid function in the DLL.  
  
3.  Isolate the procedure call causing the problem by commenting out the code. Write a `Declare` statement for the procedure, and report the problem to the type library vendor.  
  
## See Also  
 [Declare Statement](../Topic/Declare%20Statement.md)