---
title: "CRegKey::Detach"
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
ms.assetid: f95bcef9-e5a8-4db4-a879-49777ea890a3
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRegKey::Detach
Call this method to detach the [m_hKey](../vs140/CRegKey--m_hKey.md) member handle from the `CRegKey` object and set `m_hKey` to NULL.  
  
## Syntax  
  
```  
  
HKEY Detach( ) throw( );  
  
```  
  
## Return Value  
 The HKEY associated with the `CRegKey` object.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CRegKey Class](../vs140/CRegKey-Class.md)   
 [CRegKey::Attach](../vs140/CRegKey--Attach.md)