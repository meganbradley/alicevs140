---
title: "_ATL_MODULE70 Structure"
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
ms.assetid: b059b2c8-dfd1-4ac9-b07d-39df638cc7b3
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _ATL_MODULE70 Structure
Contains data used by every ATL module.  
  
## Syntax  
  
```  
  
      struct _ATL_MODULE70{  
   UINT cbSize;  
   LONG m_nLockCnt;  
   _ATL_TERMFUNC_ELEM* m_pTermFuncs;  
   CComCriticalSection m_csStaticDataInitAndTypeInfo;  
};  
```  
  
## Members  
 `cbSize`  
 The size of the structure, used for versioning.  
  
 `m_nLockCnt`  
 Reference count to determine how long the module should stay alive.  
  
 **m_pTermFuncs**  
 Tracks functions that have been registered to be called when ATL shuts down.  
  
 **m_csStaticDataInitAndTypeInfo**  
 Used to coordinate access to internal data in multithreaded situations.  
  
## Remarks  
 [_ATL_MODULE](../vs140/_ATL_MODULE.md) is defined as a typedef of `_ATL_MODULE70`.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [Structures](../vs140/ATL-Structures.md)