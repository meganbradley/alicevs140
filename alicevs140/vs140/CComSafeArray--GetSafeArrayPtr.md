---
title: "CComSafeArray::GetSafeArrayPtr"
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
ms.assetid: deef61e0-f558-4fdb-bee4-08a55e83b4cd
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComSafeArray::GetSafeArrayPtr
Returns the address of the `m_psa` data member.  
  
## Syntax  
  
```  
  
LPSAFEARRAY* GetSafeArrayPtr( ) throw( );  
  
```  
  
## Return Value  
 Returns a pointer to the [CComSafeArray::m_psa](../vs140/CComSafeArray--m_psa.md) data member.  
  
## Requirements  
 **Header:** atlsafe.h  
  
## See Also  
 [CComSafeArray Class](../vs140/CComSafeArray-Class.md)   
 [CComSafeArray::m_psa](../vs140/CComSafeArray--m_psa.md)