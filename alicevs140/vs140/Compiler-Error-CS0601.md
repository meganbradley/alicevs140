---
title: "Compiler Error CS0601"
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
ms.assetid: 20666d6f-e435-4f2d-8eca-084b7d6b57d8
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0601
The DllImport attribute must be specified on a method marked 'static' and 'extern'  
  
 The `DllImport` attribute was used on a method that did not have the correct access keywords.  
  
 The following sample generates CS0601:  
  
```  
// CS0601.cs  
using System.Runtime.InteropServices;  
using System.Text;  
  
public class C  
{  
   [DllImport("KERNEL32.DLL")]  
   extern int GetCurDirectory(int bufSize, StringBuilder buf);   // CS0601  
   // Try the following line instead:  
   // static extern int GetCurDirectory(int bufSize, StringBuilder buf);  
}  
  
public class MainClass  
{  
   public static void Main ()  
   {  
   }  
}  
```