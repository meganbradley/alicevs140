---
title: "Compiler Error CS0538"
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
ms.assetid: 46ac205e-16b0-4637-bd0f-9a755ac19f18
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0538
'name' in explicit interface declaration is not an interface  
  
 An attempt was made to explicitly declare an [interface](../vs140/interface--C#-Reference-.md), but an interface was not specified.  
  
 The following sample generates CS0538:  
  
```  
// CS0538.cs  
interface MyIFace  
{  
   void F();  
}  
  
public class MyClass  
{  
   public void G()  
   {  
   }  
}  
  
class C: MyIFace  
{  
   void MyIFace.F()  
   {  
   }  
  
   void MyClass.G()   // CS0538, MyClass not an interface  
   {  
   }  
}  
```