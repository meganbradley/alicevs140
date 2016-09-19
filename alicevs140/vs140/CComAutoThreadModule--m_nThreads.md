---
title: "CComAutoThreadModule::m_nThreads"
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
ms.assetid: c7ba1a83-0efb-4443-8d98-b19ea26debcd
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComAutoThreadModule::m_nThreads
As of ATL 7.0, `CComAutoThreadModule` is obsolete: see [ATL Module Classes](../vs140/ATL-Module-Classes.md) for more details.  
  
## Syntax  
  
```  
  
int m_nThreads;  
  
```  
  
## Remarks  
 Contains the number of threads in the EXE module. When [Init](../vs140/CComAutoThreadModule--Init.md) is called, `m_nThreads` is set to the `nThreads` parameter value. Each thread's associated apartment is managed by a [CComApartment](../vs140/CComApartment-Class.md) object.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CComAutoThreadModule Class](../vs140/CComAutoThreadModule-Class.md)   
 [CComAutoThreadModule::m_pApartments](../vs140/CComAutoThreadModule--m_pApartments.md)