---
title: "Compiler Error CS1670"
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
ms.assetid: ee2507e5-b509-4af3-a15e-2c1f2da7159c
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1670
params is not valid in this context  
  
 A number of C# features are incompatible with variable argument lists, and do not allow the `params`keyword, including the following:  
  
-   Parameter lists of anonymous methods  
  
-   Overloaded operators  
  
## Example  
 The following sample generates CS1670:  
  
```  
// CS1670.cs  
public class C  
{  
    public bool operator +(params int[] paramsList)  // CS1670  
    {  
        return false;  
    }  
  
    static void Main()  
    {  
    }  
}  
```