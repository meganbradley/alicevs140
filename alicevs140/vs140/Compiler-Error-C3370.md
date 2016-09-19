---
title: "Compiler Error C3370"
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
ms.assetid: ee6d4c85-78fc-42b2-836e-5cc491a3b2ba
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3370
'idl_module name': idl_module not yet defined  
  
 Before you can use [idl_module](../vs140/idl_module.md) to specify an entry point in a DLL, you must first use `idl_module` to specify the DLL name.  
  
 The following sample generates C3370:  
  
```  
// C3370.cpp  
[module(name=MyLibrary)];  
// uncomment the following line to resolve the error  
// [idl_module(name="name1", dllname=x.dll)];  
[idl_module(name="name1"), entry(100)] // C3370  
int f1();  
  
int main()  
{  
}  
```