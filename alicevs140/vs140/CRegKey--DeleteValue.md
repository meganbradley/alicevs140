---
title: "CRegKey::DeleteValue"
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
ms.assetid: 8fc7b57a-a73e-4275-ae0a-1263b6a99c72
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRegKey::DeleteValue
Call this method to remove a value field from [m_hKey](../vs140/CRegKey--m_hKey.md).  
  
## Syntax  
  
```  
  
      LONG DeleteValue(  
   LPCTSTR lpszValue   
) throw( );  
```  
  
#### Parameters  
 `lpszValue`  
 Specifies the value field to remove.  
  
## Return Value  
 If successful, returns ERROR_SUCCESS. If the method fails, the return value is a nonzero error code defined in WINERROR.H.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CRegKey Class](../vs140/CRegKey-Class.md)   
 [CRegKey::DeleteSubKey](../vs140/CRegKey--DeleteSubKey.md)