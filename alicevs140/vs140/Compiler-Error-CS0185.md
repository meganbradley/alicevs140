---
title: "Compiler Error CS0185"
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
ms.assetid: d6546e10-0af3-4860-8e6f-2da7dbeb3d28
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0185
'type' is not a reference type as required by the lock statement  
  
 The [lock](../Topic/lock%20Statement%20\(C%23%20Reference\).md) statement can only evaluate reference types. For more information, see [Lock Statement and Thread Synchronization (C# Programmers Reference)](../vs140/Thread-Synchronization--C#-and-Visual-Basic-.md) and [Reference Types](../vs140/Reference-Types--C#-Reference-.md).  
  
## Example  
 The following sample generates CS0185:  
  
```  
// CS0185.cs  
public class MainClass  
{  
    public static void Main ()  
    {  
        lock (1)   // CS0185  
        // try the following lines instead  
        // MainClass x = new MainClass();  
        // lock(x)  
        {  
        }  
    }  
}  
```