---
title: "CRegKey::RecurseDeleteKey"
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
ms.assetid: 8934b257-7525-4f84-b5e7-f5ab4df4b467
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRegKey::RecurseDeleteKey
Call this method to remove the specified key from the registry and explicitly remove any subkeys.  
  
## Syntax  
  
```  
  
      LONG RecurseDeleteKey(  
   LPCTSTR lpszKey   
) throw( );  
```  
  
#### Parameters  
 *lpszKey*  
 Specifies the name of the key to delete. This name must be a subkey of [m_hKey](../vs140/CRegKey--m_hKey.md).  
  
## Return Value  
 If successful, returns ERROR_SUCCESS; otherwise, a non-zero error value defined in WINERROR.H.  
  
## Remarks  
 If the key has subkeys, you must call this method to delete the key.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CRegKey Class](../vs140/CRegKey-Class.md)