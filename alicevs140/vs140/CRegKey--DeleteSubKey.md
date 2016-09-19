---
title: "CRegKey::DeleteSubKey"
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
ms.assetid: 58edbe7f-6b4a-4923-9cb5-93bfa5d2014e
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRegKey::DeleteSubKey
Call this method to remove the specified key from the registry.  
  
## Syntax  
  
```  
  
      LONG DeleteSubKey(  
   LPCTSTR lpszSubKey   
) throw( );  
```  
  
#### Parameters  
 `lpszSubKey`  
 Specifies the name of the key to delete. This name must be a subkey of [m_hKey](../vs140/CRegKey--m_hKey.md).  
  
## Return Value  
 If successful, returns ERROR_SUCCESS. If the method fails, the return value is a nonzero error code defined in WINERROR.H.  
  
## Remarks  
 `DeleteSubKey` can only delete a key that has no subkeys. If the key has subkeys, call [RecurseDeleteKey](../vs140/CRegKey--RecurseDeleteKey.md) instead.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CRegKey Class](../vs140/CRegKey-Class.md)   
 [CRegKey::DeleteValue](../vs140/CRegKey--DeleteValue.md)