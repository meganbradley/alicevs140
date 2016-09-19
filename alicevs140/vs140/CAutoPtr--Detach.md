---
title: "CAutoPtr::Detach"
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
ms.assetid: b94d7bfe-7bd7-4c39-8fda-1ddb35588ee7
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAutoPtr::Detach
Call this method to release ownership of a pointer.  
  
## Syntax  
  
```  
  
T* Detach( ) throw( );  
  
```  
  
## Return Value  
 Returns a copy of the pointer.  
  
## Remarks  
 Releases ownership of a pointer, sets the [CAutoPtr::m_p](../vs140/CAutoPtr--m_p.md) data member variable to NULL, and returns a copy of the pointer. After calling **Detach**, it is up to the programmer to free any allocated resources over which the `CAutoPtr` object may have previously assumed reponsibility.  
  
## Example  
 See the example in the [CAutoPtr Overview](../vs140/CAutoPtr-Class.md).  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CAutoPtr Class](../vs140/CAutoPtr-Class.md)   
 [CAutoPtr::Attach](../vs140/CAutoPtr--Attach.md)