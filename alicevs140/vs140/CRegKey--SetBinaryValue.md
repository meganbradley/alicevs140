---
title: "CRegKey::SetBinaryValue"
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
ms.assetid: f6887e94-8c24-4509-9c5c-d208008dc732
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRegKey::SetBinaryValue
Call this method to set the binary value of the registry key.  
  
## Syntax  
  
```  
  
      LONG SetBinaryValue(  
   LPCTSTR pszValueName,  
   const void* pValue,  
   ULONG nBytes   
) throw( );  
```  
  
#### Parameters  
 `pszValueName`  
 Pointer to a string containing the name of the value to set. If a value with this name is not already present, the method adds it to the key.  
  
 `pValue`  
 Pointer to a buffer containing the data to be stored with the specified value name.  
  
 `nBytes`  
 Specifies the size, in bytes, of the information pointed to by the `pValue` parameter.  
  
## Return Value  
 If the method succeeds, the return value is ERROR_SUCCESS. If the method fails, the return value is a nonzero error code defined in WINERROR.H.  
  
## Remarks  
 This method uses [RegSetValueEx](http://msdn.microsoft.com/library/windows/desktop/ms724923) to write the value to the registry.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CRegKey Class](../vs140/CRegKey-Class.md)   
 [CRegKey::QueryBinaryValue](../vs140/CRegKey--QueryBinaryValue.md)   
 [CRegKey::SetDWORDValue](../vs140/CRegKey--SetDWORDValue.md)   
 [CRegKey::SetQWORDValue](../vs140/CRegKey--SetQWORDValue.md)   
 [CRegKey::SetGUIDValue](../vs140/CRegKey--SetGUIDValue.md)   
 [CRegKey::SetStringValue](../vs140/CRegKey--SetStringValue.md)   
 [CRegKey::SetMultiStringValue](../vs140/CRegKey--SetMultiStringValue.md)