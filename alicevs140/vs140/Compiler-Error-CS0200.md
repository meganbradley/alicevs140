---
title: "Compiler Error CS0200"
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
ms.assetid: 1990704a-edfa-4dbd-8477-d9c7aae58c96
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0200
Property or indexer 'property' cannot be assigned to — it is read only  
  
 An attempt was made to assign a value to a [property](../vs140/Using-Properties--C#-Programming-Guide-.md), but the property does not have a set accessor. Resolve the error by adding a set accessor. For more information, see [How to: Declare and Use Read/Write Properties (C# Programmer's Reference)](../vs140/How-to--Declare-and-Use-Read-Write-Properties--C#-Programming-Guide-.md).  
  
## Example  
 The following sample generates CS0200:  
  
```  
// CS0200.cs  
public class MainClass  
{  
    // private int _mi;  
    int I  
    {  
        get  
        {  
            return 1;  
        }  
  
        // uncomment the set accessor and declaration for _mi  
        /*  
        set  
        {  
            _mi = value;  
        }  
        */  
    }  
  
    public static void Main ()  
    {  
        MainClass II = new MainClass();  
        II.I = 9;   // CS0200  
    }  
}  
```