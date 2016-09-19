---
title: "CriticalSectionTraits::GetInvalidValue Method"
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
ms.assetid: 665f30a6-ca9c-4968-8c03-8f84e6b2329b
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CriticalSectionTraits::GetInvalidValue Method
Specializes a CriticalSection template so that the template is always invalid.  
  
## Syntax  
  
```  
inline static Type GetInvalidValue();  
```  
  
## Return Value  
 Always returns a pointer to an invalid critical section.  
  
## Remarks  
 The *Type* modifier is defined as `typedef CRITICAL_SECTION* Type;`.  
  
## Requirements  
 **Header:** corewrappers.h  
  
 **Namespace:** Microsoft::WRL::Wrappers::HandleTraits  
  
## See Also  
 [CriticalSectionTraits Structure](../vs140/CriticalSectionTraits-Structure.md)