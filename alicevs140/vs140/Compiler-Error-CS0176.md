---
title: "Compiler Error CS0176"
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
ms.assetid: 783c13d8-5ac3-4aeb-bd63-0468cb05550d
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0176
Static member 'member' cannot be accessed with an instance reference; qualify it with a type name instead  
  
 Only a class name can be used to qualify a [static](../vs140/static--C#-Reference-.md) variable; an instance name cannot be a qualifier. For more information, see [Static Classes and Static Class Members (C# Programmer's Reference)](../Topic/Static%20Classes%20and%20Static%20Class%20Members%20\(C%23%20Programming%20Guide\).md).  
  
 The following sample generates CS0176:  
  
```  
// CS0176.cs  
public class MyClass2  
{  
    public static int num;  
}  
  
public class Test  
{  
    public static void Main()  
    {  
        MyClass2 mc2 = new MyClass2();  
        int i = mc2.num;   // CS0176  
        // try the following line instead  
        // int i = MyClass2.num;  
    }  
}  
  
```