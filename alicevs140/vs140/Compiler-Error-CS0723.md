---
title: "Compiler Error CS0723"
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
ms.assetid: b9f6aebc-e959-407d-8d5c-6a6dcabcfe0f
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0723
Cannot declare variable of static type 'type'  
  
 Instances of static types cannot be created.  
  
 The following sample generates CS0723:  
  
```  
// CS0723.cs  
public static class SC  
{  
}  
  
public class CMain  
{  
   public static void Main()  
   {  
      SC sc = null;  // CS0723  
   }  
}  
```