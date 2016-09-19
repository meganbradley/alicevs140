---
title: "Compiler Error C3369"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c6ceb9cb-3df9-4334-9a5c-d16db351d476
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3369
'module name': idl_module already defined  
  
 The [idl_module](../vs140/idl_module.md) usage where you define the DLL can only occur once in a program.  
  
 The following sample generates C3369:  
  
```  
// C3369.cpp  
// compile with: /c  
[idl_module(name="name1", dllname="x.dll")]; // C3369  
[idl_module(name="name1", dllname="x.dll")];  
```