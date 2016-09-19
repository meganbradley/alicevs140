---
title: "HStringReference::Operator= Operator"
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
ms.topic: reference
ms.assetid: ea100ed3-e566-4c9e-b6a8-f296088dea9c
caps.latest.revision: 4
translation.priority.ht: 
  - de-de
  - ja-jp
---
# HStringReference::Operator= Operator
Moves the value of another HStringReference object to the current HStringReference object.  
  
## Syntax  
  
```cpp  
HStringReference& operator=(HStringReference&& other) throw()  
```  
  
#### Parameters  
 `other`  
 An existing HStringReference object.  
  
## Remarks  
 The value of the existing `other` object is copied to the current HStringReference object, and then the `other` object is destroyed.  
  
## Requirements  
 **Header:** corewrappers.h  
  
 **Namespace:** Microsoft::WRL::Wrappers  
  
## See Also  
 [HStringReference Class](../vs140/HStringReference-Class.md)