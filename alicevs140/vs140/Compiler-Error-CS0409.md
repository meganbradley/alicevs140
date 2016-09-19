---
title: "Compiler Error CS0409"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 23d86c13-7978-41b7-a087-ffcea52476fa
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0409
A constraint clause has already been specified for type parameter 'type parameter'. All of the constraints for a type parameter must be specified in a single where clause.  
  
 Multiple constraint clauses (where clauses) were found for a single type parameter. Remove the extraneous where clause, or correct the where clauses so that a unique type parameter in each clause.  
  
```  
// CS0409.cs  
interface I  
{  
}  
  
class C<T1, T2> where T1 : I where T1 : I  // CS0409 – T1 used twice  
{  
}  
```