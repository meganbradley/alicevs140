---
title: "Compiler Error CS0573"
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
ms.assetid: 10ef9625-44f1-4936-ada3-56938357aa01
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0573
'field declaration' : cannot have instance field initializers in structs  
  
 You cannot initialize an instance field of a [struct](../vs140/struct--C#-Reference-.md). Fields of value types will be initialized to their default values, and reference-type fields will be initialized to `null`.  
  
## Example  
 The following sample generates CS0573:  
  
```  
// CS0573.cs  
namespace x  
{  
    public class clx  
    {  
        public static void Main()  
        {  
        }  
    }  
  
    public struct cly  
    {  
        clx a = new clx();   // CS0573  
        // clx a;            // OK  
        int i = 7;           // CS0573  
        // int i;            // OK  
    }  
}  
```