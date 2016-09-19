---
title: "Compiler Error CS0306"
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
ms.assetid: f340a3ce-6140-4001-bb00-628a2985ddd6
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0306
The type 'type' may not be used as a type argument  
  
 The type used as a type parameter is not allowed. This could be because the type is a pointer type.  
  
 The following example generates CS0306:  
  
```  
// CS0306.cs  
class C<T>  
{  
}  
  
class M  
{  
    // CS0306 – int* not allowed as a type parameter  
     C<int*> f;  
}  
```