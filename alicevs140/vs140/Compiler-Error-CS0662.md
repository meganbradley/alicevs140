---
title: "Compiler Error CS0662"
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
ms.assetid: 836fa15e-3bf3-4af5-8acf-072d7d731dcd
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0662
'method' cannot specify only Out attribute on a ref parameter. Use both In and Out attributes, or neither.  
  
 An interface method has a parameter that uses [ref](../vs140/ref--C#-Reference-.md) with just the [Out](frlrfSystemRuntimeInteropServicesOutAttributeClassTopic) attribute. A `ref` parameter that uses the **Out** attribute must also use the [In](frlrfSystemRuntimeInteropServicesInAttributeClassTopic) attribute.  
  
 The following sample generates CS0662:  
  
```  
// CS0662.cs  
using System.Runtime.InteropServices;  
  
interface I  
{  
   void method([Out] ref int i);   // CS0662  
   // try one of the following lines instead  
   // void method(ref int i);  
   // void method([Out, In]ref int i);  
}  
  
class test  
{  
   public static void Main()  
   {  
   }  
}  
```