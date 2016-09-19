---
title: "CComAutoThreadModule::m_pApartments"
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
ms.assetid: d43b4771-d20d-4f09-90e6-b051fcd38de6
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComAutoThreadModule::m_pApartments
As of ATL 7.0, `CComAutoThreadModule` is obsolete: see [ATL Module Classes](../vs140/ATL-Module-Classes.md) for more details.  
  
## Syntax  
  
```  
  
CComApartment* m_pApartments;  
  
```  
  
## Remarks  
 Points to an array of [CComApartment](../vs140/CComApartment-Class.md) objects, each of which manages an apartment in the module. The number of elements in the array is based on the [m_nThreads](../vs140/CComAutoThreadModule--m_nThreads.md) member.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CComAutoThreadModule Class](../vs140/CComAutoThreadModule-Class.md)