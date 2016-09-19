---
title: "Compiler Error CS0502"
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
ms.assetid: 6cd6deda-73a1-42d8-893b-45a685e63380
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0502
'member' cannot be both abstract and sealed  
  
 A class member cannot be both [abstract](../vs140/abstract--C#-Reference-.md) and [sealed](../vs140/sealed--C#-Reference-.md).  
  
 The following sample generates CS0502:  
  
```  
// CS0502.cs  
public class B  
{  
   abstract public void F();  
}  
  
public class C : B  
{  
   abstract sealed override public void F()   // CS0502  
   {  
   }  
}  
  
public class CMain  
{  
    public static void Main()  
    { }  
}  
```