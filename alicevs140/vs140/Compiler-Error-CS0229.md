---
title: "Compiler Error CS0229"
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
ms.topic: error-reference
ms.assetid: f1ff7e91-1243-4d36-b792-26ba69186f8f
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0229
Ambiguity between 'member1' and 'member2'  
  
 Members of different interfaces have the same name. If you want to keep the same names, you must qualify the names. For more information, see [Interfaces (C# Programmer's Reference)](../Topic/Interfaces%20\(C%23%20Programming%20Guide\).md).  
  
> [!NOTE]
>  In some cases, this ambiguity can be resolved by providing an explicit prefix to the identifier via a [using](../Topic/using%20Directive%20\(C%23%20Reference\).md) alias.  
  
## Example  
 The following example generates CS0229:  
  
```  
// CS0229.cs  
  
interface IList  
{  
    int Count  
    {  
        get;  
        set;  
    }  
  
    void Counter();  
}  
  
interface Icounter  
{  
    double Count  
    {  
        get;  
        set;  
    }  
}  
  
interface IListCounter : IList , Icounter {}  
  
class MyClass  
{  
    void Test(IListCounter x)  
    {  
        x.Count = 1;  // CS0229  
        // Try one of the following lines instead:  
        // ((IList)x).Count = 1;  
        // or  
        // ((Icounter)x).Count = 1;  
    }  
  
    public static void Main() {}  
}  
```