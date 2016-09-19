---
title: "CRegKey::QueryStringValue"
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
ms.assetid: bc80e493-c93b-48c6-9c4b-421d187f1c94
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRegKey::QueryStringValue
Call this method to retrieve the string data for a specified value name.  
  
## Syntax  
  
```  
  
      LONG QueryStringValue(  
   LPCTSTR pszValueName,  
   LPTSTR pszValue,  
   ULONG* pnChars   
) throw( );  
```  
  
#### Parameters  
 `pszValueName`  
 Pointer to a null-terminated string containing the name of the value to query.  
  
 `pszValue`  
 Pointer to a buffer that receives the string data.  
  
 `pnChars`  
 The size, in TCHARs, of the buffer pointed to by `pszValue`. When the method returns, `pnChars` contains the size, in TCHARs, of the string retrieved, including a terminating null character.  
  
## Return Value  
 If the method succeeds, ERROR_SUCCESS is returned. If the method fails to read a value, it returns a nonzero error code defined in WINERROR.H. If the data referenced is not of type REG_SZ, ERROR_INVALID_DATA is returned. If the method returns ERROR_MORE_DATA, `pnChars` equals zero, not the required buffer size in bytes.  
  
## Remarks  
 This method makes use of **RegQueryValueEx** and confirms that the correct type of data is returned. See [RegQueryValueEx](http://msdn.microsoft.com/library/windows/desktop/ms724911) for more details.  
  
> [!IMPORTANT]
>  This method allows the caller to specify any registry location, potentially reading data which cannot be trusted. Also, the [RegQueryValueEx](http://msdn.microsoft.com/library/windows/desktop/ms724911) function used by this method does not explicitly handle strings which are NULL terminated. Both conditions should be checked for by the calling code.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CRegKey Class](../vs140/CRegKey-Class.md)   
 [CRegKey::SetStringValue](../vs140/CRegKey--SetStringValue.md)   
 [CRegKey::QueryBinaryValue](../vs140/CRegKey--QueryBinaryValue.md)   
 [CRegKey::QueryDWORDValue](../vs140/CRegKey--QueryDWORDValue.md)   
 [CRegKey::QueryGUIDValue](../vs140/CRegKey--QueryGUIDValue.md)   
 [CRegKey::QueryMultiStringValue](../vs140/CRegKey--QueryMultiStringValue.md)   
 [CRegKey::QueryQWORDValue](../vs140/CRegKey--QueryQWORDValue.md)