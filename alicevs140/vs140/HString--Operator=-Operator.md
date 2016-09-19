---
title: "HString::Operator= Operator"
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
ms.assetid: 8e68c1ff-bc57-4526-810e-af3c284b4e30
caps.latest.revision: 4
translation.priority.ht: 
  - de-de
  - ja-jp
---
# HString::Operator= Operator
Moves the value of another HString object to the current HString object.  
  
## Syntax  
  
```cpp  
HString& operator=(HString&& other) throw()  
```  
  
#### Parameters  
 `other`  
 An existing HString object.  
  
## Remarks  
 The value of the existing `other` object is copied to the current HString object, and then the `other` object is destroyed.  
  
## Requirements  
 **Header:** corewrappers.h  
  
 **Namespace:** Microsoft::WRL::Wrappers  
  
## See Also  
 [HString Class](../vs140/HString-Class.md)