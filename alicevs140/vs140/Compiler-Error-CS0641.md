---
title: "Compiler Error CS0641"
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
ms.assetid: 5bcdb11a-fefd-4c71-9b31-4c4f719633f3
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0641
'attribute' : attribute is only valid on classes derived from System.Attribute  
  
 An attribute was used that can only be used on a class that derives from **System.Attribute**.  
  
 The following sample generates CS0641:  
  
```  
// CS0641.cs  
using System;  
  
[AttributeUsage(AttributeTargets.All)]  
public class NonAttrClass   // CS0641  
// try the following line instead  
// public class NonAttrClass : Attribute  
{  
}  
  
class MyClass  
{  
   public static void Main()  
   {  
   }  
}  
```