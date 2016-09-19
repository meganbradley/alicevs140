---
title: "Compiler Warning (level 2) CS0458"
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
ms.assetid: 0986c620-b4bc-4e4b-976f-88359cfa3a45
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 2) CS0458
The result of the expression is always 'null' of type 'type name'  
  
 This warning is caused by a `nullable` expression that always results in `null`.  
  
 The following code generates warning CS0458.  
  
## Example  
 This example illustrates a number of the different operations with `nullable` types that will cause this error.  
  
```  
// CS0458.cs  
using System;  
public  class Test   
{  
    public static void Main()  
    {  
        int a = 5;  
        int? b = a + null;    // CS0458  
        int? qa = 15;  
        b = qa + null;        // CS0458  
        b -= null;            // CS0458  
        int? qa2 = null;  
        b = qa2 + null;       // CS0458  
        qa2 -= null;          // CS0458  
    }  
}  
```