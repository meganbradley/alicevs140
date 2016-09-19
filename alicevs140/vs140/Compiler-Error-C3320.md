---
title: "Compiler Error C3320"
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
ms.assetid: 2ef72d9a-1f1d-4b2e-b244-9fd3f3e70cb6
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3320
'type': type cannot have the same name as the module 'name' property  
  
 An exported user-defined type (UDT), which could be a struct, class, enum, union or [__value](../vs140/__value.md), cannot have the same name as the parameter passed to the [module](../vs140/module--C---.md) attribute's name property.  
  
 The following sample generates C3320:  
  
```  
// C3320.cpp  
#include "unknwn.h"  
[module(name="xx")];  
  
[export] struct xx {   // C3320  
// Try the following line instead  
// [export] struct yy {  
   int i;  
};  
```