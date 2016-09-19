---
title: "virtual (C++)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: language-reference
ms.assetid: c2eb987d-6cf3-43b6-aa0c-29a6f561b1ae
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# virtual (C++)
The `virtual` keyword declares a virtual function or a virtual base class.  
  
## Syntax  
  
```  
virtual [type-specifiers] member-function-declarator  
virtual [access-specifier] base-class-name  
```  
  
#### Parameters  
 `type-specifiers`  
 Specifies the return type of the virtual member function.  
  
 `member-function-declarator`  
 Declares a member function.  
  
 `access-specifier`  
 Defines the level of access to the base class, `public`, `protected` or `private`. Can appear before or after the `virtual` keyword.  
  
 `base-class-name`  
 Identifies a previously declared class type.  
  
## Remarks  
 See [Virtual Functions](../vs140/Virtual-Functions.md) and [Virtual Base Classes](../vs140/Virtual-Base-Classes.md) for more information.  
  
 Also see the following keywords: [class](../vs140/class--C---.md), [private](../vs140/private--C---.md), [public](../vs140/public--C---.md), and [protected](../vs140/protected--C---.md).  
  
## See Also  
 [Keywords](../vs140/Keywords--C---.md)