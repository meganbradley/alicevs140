---
title: "Compiler Error CS1650"
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
ms.assetid: 251a3a67-6e56-4795-874a-d54610c70595
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1650
Fields of static readonly field 'identifier' cannot be assigned to (except in a static constructor or a variable initializer)  
  
 This error occurs when you attempt to modify a member of a field which is readonly and static where it is not allowed to be modified. To resolve this error, limit assignments to readonly fields to the constructor or variable initializer, or remove the `readonly` keyword from the declaration of the field.  
  
```  
// CS1650.cs  
public struct Inner  
{  
    public int i;  
}  
  
class Outer  
{  
    public static readonly Inner inner = new Inner();  
}  
  
class D  
{  
    static void Main()  
    {  
        Outer.inner.i = 1;  // CS1650  
    }  
}  
```