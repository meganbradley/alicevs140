---
title: "Compiler Error CS1038"
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
ms.assetid: 05c53ae9-2819-4771-aee8-3f2ff6bcf0b0
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1038
\#endregion directive expected  
  
 A [#region](../vs140/#region--C#-Reference-.md) directive did not have a matching [#endregion](../vs140/#endregion--C#-Reference-.md) directive.  
  
 The following sample generates CS1038:  
  
```  
// CS1038.cs  
#region testing  
  
public class clx  
{  
   public static void Main()  
   {  
   }  
}  
// CS1038  
// uncomment the next line to resolve  
// #endregion  
```