---
title: "Compiler Error CS0058"
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
ms.assetid: 9535da60-03b9-41ab-93e1-e57b6440fca9
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0058
Inconsistent accessibility: return type 'type' is less accessible than delegate 'delegate'  
  
 A public construct must return a publicly accessible object. For more information, see [Access Modifiers (C# Programmers Reference)](../Topic/Access%20Modifiers%20\(C%23%20Programming%20Guide\).md).  
  
 The following sample generates CS0058 because no access modifier is applied to MyClass and therefore it is given private accessibility by default:  
  
```  
// CS0058.cs  
class MyClass  
// try the following line instead  
// public class MyClass  
{  
}  
  
public delegate MyClass MyClassDel();   // CS0058  
  
public class A  
{  
   public static void Main()  
   {  
   }  
}  
```  
  
## See Also  
 [private (C# Programmer's Reference)](../vs140/private--C#-Reference-.md)