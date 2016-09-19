---
title: "Compiler Error CS0719"
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
ms.assetid: 308a1a54-43b9-4970-8206-88e8f76d394e
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0719
'type': array elements cannot be of static type  
  
 An array of static type does not make sense since array elements are instances, but it is not possible to create instances of static types.  
  
 The following sample generates CS0719:  
  
```  
// CS0719.cs  
public static class SC  
{  
   public static void F()  
   {  
   }  
}  
  
public class CMain  
{  
   public static void Main()  
   {  
      SC[] sca = new SC[10];  // CS0719  
   }  
}  
```