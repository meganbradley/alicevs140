---
title: "Mutex::operator= Operator"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: 9b0ee206-a930-4fea-8dc0-1f79839e9d13
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Mutex::operator= Operator
Assigns (moves) the specified Mutex object to the current Mutex object.  
  
## Syntax  
  
```  
Mutex& operator=(  
   _Inout_ Mutex&& h  
);  
```  
  
#### Parameters  
 `h`  
 An rvalue-reference to a Mutex object.  
  
## Return Value  
 A reference to the current Mutex object.  
  
## Remarks  
 For more information, see the **Move Semantics** section of [Rvalue Reference Declarator: &&](../vs140/Rvalue-Reference-Declarator----.md).  
  
## Requirements  
 **Header:** corewrappers.h  
  
 **Namespace:** Microsoft::WRL::Wrappers  
  
## See Also  
 [Mutex Class](../vs140/Mutex-Class.md)