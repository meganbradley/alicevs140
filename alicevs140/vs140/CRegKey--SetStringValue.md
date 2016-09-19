---
title: "CRegKey::SetStringValue"
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
ms.assetid: e2c558ae-ee64-4a5a-914b-fec3a92def97
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRegKey::SetStringValue
Call this method to set the string value of the registry key.  
  
## Syntax  
  
```  
LONG SetStringValue(  
   LPCTSTR pszValueName,  
   LPCTSTR pszValue,  
   DWORD dwType = REG_SZ   
) throw( );  
```  
  
#### Parameters  
 `pszValueName`  
 Pointer to a string containing the name of the value to set. If a value with this name is not already present, the method adds it to the key.  
  
 `pszValue`  
 Pointer to the string data to be stored with the specified value name.  
  
 `dwType`  
 The type of the string to write to the registry: either REG_SZ (the default) or REG_EXPAND_SZ (for multistrings).  
  
## Return Value  
 If the method succeeds, the return value is ERROR_SUCCESS. If the method fails, the return value is a nonzero error code defined in WINERROR.H.  
  
## Remarks  
 This method uses [RegSetValueEx](http://msdn.microsoft.com/library/windows/desktop/ms724923\(v=vs.85\).aspx) to write the value to the registry.  
  
## Requirements  
 Header: atlbase.h  
  
## See Also  
 [CRegKey Class](../vs140/CRegKey-Class.md)   
 [CRegKey::QueryStringValue](../vs140/CRegKey--QueryStringValue.md)   
 [CRegKey::SetDWORDValue](../vs140/CRegKey--SetDWORDValue.md)   
 [CRegKey::SetQWORDValue](../vs140/CRegKey--SetQWORDValue.md)   
 [CRegKey::SetGUIDValue](../vs140/CRegKey--SetGUIDValue.md)   
 [CRegKey::SetMultiStringValue](../vs140/CRegKey--SetMultiStringValue.md)   
 [CRegKey::SetBinaryValue](../vs140/CRegKey--SetBinaryValue.md)