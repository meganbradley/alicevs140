---
title: "CAutoPtr::Free"
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
ms.assetid: e9bc7840-2df9-454d-9bb6-81cbb1be2361
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAutoPtr::Free
Call this method to delete an object pointed to by a `CAutoPtr`.  
  
## Syntax  
  
```  
  
void Free( ) throw( );  
  
```  
  
## Remarks  
 The object pointed to by the `CAutoPtr` is freed, and the [CAutoPtr::m_p](../vs140/CAutoPtr--m_p.md) data member variable is set to NULL.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CAutoPtr Class](../vs140/CAutoPtr-Class.md)