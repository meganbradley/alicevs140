---
title: "CRegKey::Attach"
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
ms.assetid: 02246d9d-4a2a-4542-93bc-7a9d44800013
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRegKey::Attach
Call this method to attach an HKEY to the `CRegKey` object by setting the [m_hKey](../vs140/CRegKey--m_hKey.md) member handle to `hKey`.  
  
## Syntax  
  
```  
  
      void Attach(  
   HKEY hKey   
) throw( );  
```  
  
#### Parameters  
 `hKey`  
 The handle of a registry key.  
  
## Remarks  
 **Attach** will assert if `m_hKey` is non-NULL.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CRegKey Class](../vs140/CRegKey-Class.md)   
 [CRegKey::Detach](../vs140/CRegKey--Detach.md)