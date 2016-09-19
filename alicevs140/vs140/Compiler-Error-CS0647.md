---
title: "Compiler Error CS0647"
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
ms.assetid: b62d7fc9-4711-428e-ab66-09ea1c9970f0
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0647
Error emitting 'attribute' attribute -- 'reason'  
  
 The following sample generates CS0647:  
  
```  
// CS0647.cs  
using System.Runtime.InteropServices;  
  
[Guid("z")]   // CS0647, incorrect uuid format.  
// try the following line instead  
// [Guid("00000000-0000-0000-0000-000000000001")]  
public class MyClass  
{  
   public static void Main()  
   {  
   }  
}  
```