---
title: "Compiler Error CS0596"
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
ms.assetid: 7cbf0db1-bb0b-4c50-b71e-16599a7e37d0
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0596
The Guid attribute must be specified with the ComImport attribute  
  
 The **Guid** attribute must be present when using the **ComImport** attribute.  
  
 The following sample generates CS0596:  
  
```  
// CS0596.cs  
using System.Runtime.InteropServices;  
  
namespace x  
{  
   [ComImport]   // CS0596  
   // try the following line to resolve this CS0596  
   // [ComImport, Guid("00000000-0000-0000-0000-000000000001")]  
   public class a  
   {  
   }  
  
   public class b  
   {  
      public static void Main()  
      {  
      }  
   }  
}  
```