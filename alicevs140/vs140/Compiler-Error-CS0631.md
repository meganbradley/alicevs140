---
title: "Compiler Error CS0631"
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
ms.assetid: 5ae06b13-7874-4d0d-b256-7d8b33396156
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0631
ref and out are not valid in this context  
  
 The declaration for an [indexer](../vs140/Indexers--C#-Programming-Guide-.md) cannot include the use of [ref](../vs140/ref--C#-Reference-.md) or [out](../vs140/out--C#-Reference-.md) parameters.  
  
## Example  
 The following sample generates CS0631:  
  
```  
// CS0631.cs  
public class MyClass  
{  
    public int this[ref int i]   // CS0631  
    // try the following line instead  
    // public int this[int i]  
    {  
        get  
        {  
            return 0;  
        }  
    }  
}  
  
public class MyClass2  
{  
    public static void Main()  
    {  
    }  
}  
```