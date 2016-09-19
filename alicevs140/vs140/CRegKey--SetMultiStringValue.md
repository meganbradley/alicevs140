---
title: "CRegKey::SetMultiStringValue"
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
ms.assetid: d5ec045b-9708-4341-add1-689ff4ddf44f
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRegKey::SetMultiStringValue
Call this method to set the multistring value of the registry key.  
  
## Syntax  
  
```  
  
      LONG SetMultiStringValue(  
   LPCTSTR pszValueName,  
   LPCTSTR pszValue   
) throw( );  
```  
  
#### Parameters  
 `pszValueName`  
 Pointer to a string containing the name of the value to set. If a value with this name is not already present, the method adds it to the key.  
  
 `pszValue`  
 Pointer to the multistring data to be stored with the specified value name. A multistring is an array of null-terminated strings, terminated by two null characters.  
  
## Return Value  
 If the method succeeds, the return value is ERROR_SUCCESS. If the method fails, the return value is a nonzero error code defined in WINERROR.H.  
  
## Remarks  
 This method uses [RegSetValueEx](http://msdn.microsoft.com/library/windows/desktop/ms724923) to write the value to the registry.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CRegKey Class](../vs140/CRegKey-Class.md)   
 [CRegKey::QueryMultiStringValue](../vs140/CRegKey--QueryMultiStringValue.md)   
 [CRegKey::SetDWORDValue](../vs140/CRegKey--SetDWORDValue.md)   
 [CRegKey::SetQWORDValue](../vs140/CRegKey--SetQWORDValue.md)   
 [CRegKey::SetGUIDValue](../vs140/CRegKey--SetGUIDValue.md)   
 [CRegKey::SetStringValue](../vs140/CRegKey--SetStringValue.md)   
 [CRegKey::SetBinaryValue](../vs140/CRegKey--SetBinaryValue.md)