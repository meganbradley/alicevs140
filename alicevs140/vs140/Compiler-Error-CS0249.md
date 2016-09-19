---
title: "Compiler Error CS0249"
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
ms.assetid: 8bc3572f-d949-4867-b119-6527fb924a4a
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0249
Do not override object.Finalize. Instead, provide a destructor.  
  
 Use destructor syntax to specify instructions to execute when your object is destroyed.  
  
 For more information, see [Destructor Syntax in C# and C++](assetId:///d7901491-7e89-4b6f-8270-0635aa6581b5).  
  
 The following sample generates CS0249:  
  
```  
// CS0249.cs  
class MyClass  
{  
   protected override void Finalize()   // CS0249  
   // try the following line instead  
   // ~MyClass()  
   {  
   }  
  
   public static void Main()  
   {  
   }  
}  
```