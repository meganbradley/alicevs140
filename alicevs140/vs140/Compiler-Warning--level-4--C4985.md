---
title: "Compiler Warning (level 4) C4985"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 832f001c-afe7-403d-a8b4-02334724c79e
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 4) C4985
'symbol name': attributes not present on previous declaration.  
  
 The Microsoft source code annotation language (SAL) annotations on the current method declaration or definition differ from the annotations on an earlier declaration. The same SAL annotations must be used in the definition and declarations of a method.  
  
 The SAL provides a set of annotations that you can use to describe how a function uses its parameters, the assumptions it makes about them, and the guarantees it makes on finishing. The annotations are defined in the sal.h header file.  
  
 Notice that the SAL macros will not expand unless the project has the [/analyze](../Topic/-analyze%20\(Code%20Analysis\).md) flag specified. When you specify **/analyze**, the compiler can throw C4985, even if no warnings or errors appeared without **/analyze**.  
  
### To correct this error  
  
1.  Use the same SAL annotations on the definition of a method and all its declarations.  
  
## See Also  
 [SAL Annotations](../vs140/SAL-Annotations.md)