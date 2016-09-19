---
title: "Compiler Error CS0541"
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
ms.assetid: ed812c07-24f7-43c6-9a44-553f27f6249d
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0541
'declaration' : explicit interface declaration can only be declared in a class or struct  
  
 An explicit [interface](../vs140/interface--C#-Reference-.md) declaration was found outside a [class](../vs140/class--C#-Reference-.md) or [struct](../vs140/struct--C#-Reference-.md).  
  
 The following sample generates CS0541:  
  
```  
// CS0541.cs  
namespace x  
{  
   interface IFace  
   {  
      void F();  
   }  
  
   interface IFace2 : IFace  
   {  
      void IFace.F();   // CS0541  
   }  
}  
```