---
title: "Compiler Error CS0065"
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
ms.assetid: 49ca30a8-513a-40ed-aa0c-eb696a25b91f
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0065
'event' : event property must have both add and remove accessors  
  
 An event that is not a field must have both access methods.  
  
 The following sample generates CS0065:  
  
```  
// CS0065.cs  
using System;  
public delegate void Eventhandler(object sender, int e);  
public class MyClass  
{  
   public event EventHandler Click   // CS0065,  
   {  
      // to fix, uncomment the add and remove definitions  
      /*  
      add  
      {  
         Click += value;  
      }  
      remove  
      {  
         Click -= value;  
      }  
      */  
   }  
  
   public static void Main()  
   {  
   }  
}  
```  
  
## See Also  
 [Events (C# Programmers Reference)](../Topic/Events%20\(C%23%20Programming%20Guide\).md)