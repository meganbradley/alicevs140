---
title: "_ATL_WIN_MODULE70 Structure"
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
ms.topic: article
ms.assetid: a0aaf3ea-ca77-46ec-bd53-4dfb61dffbea
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _ATL_WIN_MODULE70 Structure
Used by windowing code in ATL.  
  
## Syntax  
  
```  
  
      struct _ATL_WIN_MODULE70{  
   UNIT cbSize;  
   CRITICAL_SECTION m_csWindowCreate;  
   _AtlCreateWndData* m_pCreateWndList;  
   CSimpleArray<ATOM> m_rgWindowClassAtoms;  
};  
```  
  
## Members  
 `cbSize`  
 The size of the structure, used for versioning.  
  
 `m_csWindowCreate`  
 Used to serialize access to window registration code. Used internally by ATL.  
  
 **m_pCreateWndList**  
 Used to bind windows to their objects. Used internally by ATL.  
  
 **m_rgWindowClassAtoms**  
 Used to track window class registrations so that they can be properly unregistered at termination. Used internally by ATL.  
  
## Remarks  
 [_ATL_WIN_MODULE](../vs140/_ATL_WIN_MODULE.md) is defined as a typedef of `_ATL_WIN_MODULE70`.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [Structures](../vs140/ATL-Structures.md)