---
title: "Compiler Error C3347"
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
ms.assetid: e939ad29-0b78-4681-9618-9bdae5675cee
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3347
'arg': required argument is not specified in attribute idl_module  
  
 A required argument was not passed to the [idl_module](../vs140/idl_module.md) attribute.  
  
 The following sample generates C3347:  
  
```  
// C3347.cpp  
// compile with: /c  
[module(name="xx")];  
  
[idl_module(dllname="x")];    // C3347  
// try the following line instead  
// [idl_module(name="test", dllname="x")];  
```