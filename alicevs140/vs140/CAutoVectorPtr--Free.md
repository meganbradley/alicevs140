---
title: "CAutoVectorPtr::Free"
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
ms.assetid: 24ef7ee0-6d5b-4ed8-972e-ae9440e04b6e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAutoVectorPtr::Free
Call this method to delete an object pointed to by a `CAutoVectorPtr`.  
  
## Syntax  
  
```  
  
void Free( ) throw( );  
  
```  
  
## Remarks  
 The object pointed to by the `CAutoVectorPtr` is freed, and the [CAutoVectorPtr::m_p](../vs140/CAutoVectorPtr--m_p.md) member variable is set to NULL.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CAutoVectorPtr Class](../vs140/CAutoVectorPtr-Class.md)