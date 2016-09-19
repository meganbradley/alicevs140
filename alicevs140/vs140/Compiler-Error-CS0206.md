---
title: "Compiler Error CS0206"
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
ms.assetid: d2f9838a-d8ae-4342-b8bd-fa5745619a26
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0206
A property or indexer may not be passed as an out or ref parameter  
  
 A [property](../vs140/Properties--C#-Programming-Guide-.md) is not available to be passed as a [ref](../vs140/ref--C#-Reference-.md) or [out](../vs140/out--C#-Reference-.md) parameter. For more information, see [Passing Parameters (C# Programmer's Reference)](../vs140/Passing-Parameters--C#-Programming-Guide-.md).  
  
## Example  
 The following sample generates CS0206:  
  
```  
// CS0206.cs  
public class MyClass  
{  
    public static int P  
    {  
        get  
        {  
            return 0;  
        }  
        set  
        {  
        }  
    }  
  
    public static void MyMeth(ref int i)  
    // public static void MyMeth(int i)  
    {  
    }  
  
    public static void Main()  
    {  
        MyMeth(ref P);   // CS0206  
        // try the following line instead  
        // MyMeth(P);   // CS0206  
    }  
}  
```