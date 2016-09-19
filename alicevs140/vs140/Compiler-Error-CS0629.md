---
title: "Compiler Error CS0629"
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
ms.assetid: 20f22ef0-3c6f-4108-ab09-3f0752375a10
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0629
Conditional member 'member' cannot implement interface member 'base class member' in type 'Type Name'  
  
 The [Conditional](assetId:///e1c4913b-74d0-421a-8a6d-c14b3f0e68fb) attribute cannot be used on the implementation of an interface.  
  
 The following sample generates CS0629:  
  
```  
// CS0629.cs  
interface MyInterface  
{  
   void MyMethod();  
}  
  
public class MyClass : MyInterface  
{  
   [System.Diagnostics.Conditional("debug")]  
   public void MyMethod()    // CS0629, remove the Conditional attribute  
   {  
   }  
  
   public static void Main()  
   {  
   }  
}  
```