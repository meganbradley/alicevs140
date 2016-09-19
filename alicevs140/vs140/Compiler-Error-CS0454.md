---
title: "Compiler Error CS0454"
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
ms.assetid: 2c83bc5e-53bb-473e-92aa-5122dadd79d1
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0454
Circular constraint dependency involving 'Type Parameter 1' and 'Type Parameter 2'  
  
 This error arises because at some point one type parameter refers to another, and the second refers back to the first. To fix this error, break the circular dependency by removing one of the constraints. Note that the circular constraint dependency can be indirect.  
  
## Example  
 The following code generates error CS0454.  
  
```  
// CS0554  
using System;  
public class GenericsErrors   
{  
    public class G4<T> where T : T { } // CS0454  
}  
```  
  
## Example  
 The following example demonstrates a circular dependency between two type constraints.  
  
```  
public class Gen<T,U> where T : U where U : T  // CS0454  
{  
}  
```