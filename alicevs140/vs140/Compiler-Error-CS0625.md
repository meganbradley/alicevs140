---
title: "Compiler Error CS0625"
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
ms.assetid: 44091813-9988-436c-b35e-e24094793782
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0625
'field': instance field types marked with StructLayout(LayoutKind.Explicit) must have a FieldOffset attribute  
  
 When a struct is marked with an explicit **StructLayout** attribute, all fields in the struct must have the [FieldOffset](frlrfsystemruntimeinteropservicesfieldoffsetattributeclasstopic) attribute. For more information, see [StructLayoutAttribute Class](frlrfSystemRuntimeInteropServicesStructLayoutAttributeClassTopic).  
  
 The following sample generates CS0625:  
  
```  
// CS0625.cs  
// compile with: /target:library  
using System;  
using System.Runtime.InteropServices;  
  
[StructLayout(LayoutKind.Explicit)]  
struct A  
{  
   public int i;   // CS0625 not static; an instance field  
}  
  
// OK  
[StructLayout(LayoutKind.Explicit)]  
struct B  
{  
   [FieldOffset(5)]  
   public int i;  
}  
```