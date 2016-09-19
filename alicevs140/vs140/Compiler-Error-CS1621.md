---
title: "Compiler Error CS1621"
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
ms.assetid: 11b4fb94-0dd7-4484-99aa-e06eacc6a658
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1621
The yield statement cannot be used inside an anonymous method or lambda expression  
  
 The yield statement cannot be in an anonymous method block in an iterator.  
  
## Example  
 The following sample generates CS1621:  
  
```  
// CS1621.cs  
  
using System.Collections;  
  
delegate object MyDelegate();  
  
class C : IEnumerable  
{  
    public IEnumerator GetEnumerator()  
    {  
        MyDelegate d = delegate  
        {  
            yield return this; // CS1621  
            return this;  
        };  
        d();  
        // Try this instead:  
        // MyDelegate d = delegate { return this; };  
        // yield return d();  
    }  
  
    public static void Main()  
    {  
    }  
}  
```  
  
## See Also  
 [Iterators (C# Programming Guide)](../vs140/Iterators--C#-and-Visual-Basic-.md)   
 [yield](../Topic/yield%20\(C%23%20Reference\).md)   
 [Lambda Expressions (C# Programming Guide)](../Topic/Lambda%20Expressions%20\(C%23%20Programming%20Guide\).md)   
 [Anonymous Methods (C# Programming Guide)](../vs140/Anonymous-Methods--C#-Programming-Guide-.md)