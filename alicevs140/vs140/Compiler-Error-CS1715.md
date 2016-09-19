---
title: "Compiler Error CS1715"
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
ms.assetid: 740044d1-a61c-4156-bc6a-adf26c7499ec
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1715
'Type1': type must be 'Type2' to match overridden member 'MemberName'  
  
 This error is the same as [Compiler Error CS0508](../vs140/Compiler-Error-CS0508.md), except that CS0508 now only applies to methods that have return types, while CS1715 applies to properties and indexers that only have 'types' instead of 'return types'.  
  
## Example  
 The following code generates CS1715.  
  
```  
// CS1715.cs  
abstract public class Base  
{  
    abstract public int myProperty  
    {  
        get;  
        set;  
    }  
}  
  
public class Derived : Base  
{  
    int myField;  
    public override double myProperty  // CS1715  
    // try the following line instead  
    // public override int myProperty  
    {  
        get { return myField; }  
        set { myField;= value; }  
    }  
  
    public static void Main()  
    {  
        Derived d = new Derived();  
        d.myProperty = 5;  
    }  
}  
```