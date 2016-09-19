---
title: "HString::GetAddressOf Method"
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
ms.assetid: 6050decf-5f99-49f0-9497-1c8192c485ae
caps.latest.revision: 4
translation.priority.ht: 
  - de-de
  - ja-jp
---
# HString::GetAddressOf Method
Retrieves a pointer to the underlying HSTRING handle.  
  
## Syntax  
  
```  
HSTRING* GetAddressOf() throw()  
```  
  
## Return Value  
 A pointer to the underlying HSTRING handle.  
  
## Remarks  
 After this operation, the string value of the underlying HSTRING handle is destroyed.  
  
## Requirements  
 **Header:** corewrappers.h  
  
 **Namespace:** Microsoft::WRL::Wrappers  
  
## See Also  
 [HString Class](../vs140/HString-Class.md)