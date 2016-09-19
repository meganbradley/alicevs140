---
title: "Compiler Error CS1007"
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
ms.assetid: b56ee2c6-8e79-4b9b-8c59-194bdb22bc3e
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1007
Property accessor already defined  
  
 When you declare a [property](../vs140/Using-Properties--C#-Programming-Guide-.md), you must also declare its accessor methods. However, a property cannot have more than one `get` accessor method or more than one `set` accessor method.  
  
## Example  
 The following sample generates CS1007:  
  
```  
// CS1007.cs  
public class clx  
{  
    public int MyProperty  
    {  
        get  
        {  
            return 0;  
        }  
        get   // CS1007, this is the second get method  
        {  
            return 0;  
        }  
    }  
  
    public static void Main() {}  
}  
```