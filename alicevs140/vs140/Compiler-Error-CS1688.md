---
title: "Compiler Error CS1688"
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
ms.assetid: e15672a1-2570-4e65-99fc-7acc190ae643
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1688
Cannot convert anonymous method block without a parameter list to delegate type 'delegate' because it has one or more out parameters  
  
 The compiler allows parameters to be omitted from an anonymous method block in most cases. This error arises when the anonymous method block does not have a parameter list, but the delegate has an `out` parameter. The compiler does not allow this situation because it would need to ignore the presence of the `out` parameter, which is unlikely to be the correct behavior.  
  
## Example  
 The following code generates error CS1688.  
  
```  
// CS1688.cs  
using System;  
delegate void OutParam(out int i);  
class ErrorCS1676  
{  
    static void Main()   
    {  
        OutParam o;  
        o = delegate  // CS1688  
        // Try this instead:  
        // o = delegate(out int i)  
        {   
            Console.WriteLine("");  
        };  
    }  
}  
```