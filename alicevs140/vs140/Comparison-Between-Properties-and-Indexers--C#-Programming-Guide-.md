---
title: "Comparison Between Properties and Indexers (C# Programming Guide)"
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
ms.assetid: 3358a89f-44a0-4a4d-bf8c-07237a90af39
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Comparison Between Properties and Indexers (C# Programming Guide)
Indexers are like properties. Except for the differences shown in the following table, all the rules that are defined for property accessors apply to indexer accessors also.  
  
|Property|Indexer|  
|--------------|-------------|  
|Allows methods to be called as if they were public data members.|Allows elements of an internal collection of an object to be accessed by using array notation on the object itself.|  
|Accessed through a simple name.|Accessed through an index.|  
|Can be a static or an instance member.|Must be an instance member.|  
|A [get](../vs140/get--C#-Reference-.md) accessor of a property has no parameters.|A `get` accessor of an indexer has the same formal parameter list as the indexer.|  
|A [set](../vs140/set--C#-Reference-.md) accessor of a property contains the implicit `value` parameter.|A `set` accessor of an indexer has the same formal parameter list as the indexer, and also to the [value](../vs140/value--C#-Reference-.md) parameter.|  
|Supports shortened syntax with [Auto-Implemented Properties (C# Programming Guide)](../vs140/Auto-Implemented-Properties--C#-Programming-Guide-.md).|Does not support shortened syntax.|  
  
## See Also  
 [C# Programming](../vs140/C#-Programming-Guide.md)   
 [Indexers](../vs140/Indexers--C#-Programming-Guide-.md)   
 [Properties](../vs140/Properties--C#-Programming-Guide-.md)