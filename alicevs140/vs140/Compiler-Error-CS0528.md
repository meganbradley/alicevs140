---
title: "Compiler Error CS0528"
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
ms.assetid: 8f5dde55-7e4f-4ffa-be14-0e0f3a538118
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0528
'interface' is already listed in interface list  
  
 An interface-inheritance list includes a duplicate. An [interface](../vs140/interface--C#-Reference-.md) can only be specified once in the inheritance list.  
  
 The following sample generates CS0528:  
  
```  
// CS0528.cs  
namespace x  
{  
   public interface a  
   {  
   }  
  
   public class b : a, a   // CS0528  
   {  
      public void Main()  
      {  
      }  
   }  
}  
```