---
title: "Compiler Error CS0724"
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
ms.assetid: bcdb2017-7a43-4242-b4e2-a1ae03d6d73f
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0724
does not need a CLSCompliant attribute because the assembly does not have a CLSCompliant attribute  
  
 The following example generates CS0724 because of the `throw` statement inside the `finally` clause block.  
  
## Example  
 The following example generates CS0724.  
  
```  
// CS0724.cs  
using System;  
  
class X  
{  
    static void Test()  
    {  
        try  
        {  
            throw new Exception();  
        }  
        catch  
        {  
            try  
            {  
            }  
            finally  
            {  
                throw; // CS0724  
            }  
        }  
    }  
  
    static void Main()  
    {  
    }  
}  
```