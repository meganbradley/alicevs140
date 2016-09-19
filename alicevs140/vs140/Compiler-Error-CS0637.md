---
title: "Compiler Error CS0637"
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
ms.assetid: 02f6964c-0fcc-4f81-8ebb-0330aecdde19
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0637
The FieldOffset attribute is not allowed on static or const fields  
  
 The [FieldOffset](frlrfsystemruntimeinteropservicesfieldoffsetattributeclasstopic) attribute cannot be used on fields marked with [static](../vs140/static--C#-Reference-.md) or [const](../vs140/const--C#-Reference-.md).  
  
 The following sample generates CS0637:  
  
```  
// CS0637.cs  
using System;  
using System.Runtime.InteropServices;  
  
[StructLayout(LayoutKind.Explicit)]  
public class MainClass  
{  
   [FieldOffset(3)]   // CS0637  
   public static int i;  
   public static void Main ()  
   {  
   }  
}  
```