---
title: "CRegKey::QueryMultiStringValue"
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
ms.assetid: 278c2494-d805-4fc7-bbdd-c1d983e7d765
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRegKey::QueryMultiStringValue
Call this method to retrieve the multistring data for a specified value name.  
  
## Syntax  
  
```  
  
      LONG QueryMultiStringValue(  
   LPCTSTR pszValueName,  
   LPTSTR pszValue,  
   ULONG* pnChars   
) throw( );  
```  
  
#### Parameters  
 `pszValueName`  
 Pointer to a null-terminated string containing the name of the value to query.  
  
 `pszValue`  
 Pointer to a buffer that receives the multistring data. A multistring is an array of null-terminated strings, terminated by two null characters.  
  
 `pnChars`  
 The size, in TCHARs, of the buffer pointed to by `pszValue`. When the method returns, `pnChars` contains the size, in TCHARs, of the multistring retrieved, including a terminating null character.  
  
## Return Value  
 If the method succeeds, ERROR_SUCCESS is returned. If the method fails to read a value, it returns a nonzero error code defined in WINERROR.H. If the data referenced is not of type REG_MULTI_SZ, ERROR_INVALID_DATA is returned.  
  
## Remarks  
 This method makes use of **RegQueryValueEx** and confirms that the correct type of data is returned. See [RegQueryValueEx](http://msdn.microsoft.com/library/windows/desktop/ms724911) for more details.  
  
> [!IMPORTANT]
>  This method allows the caller to specify any registry location, potentially reading data which cannot be trusted. Also, the [RegQueryValueEx](http://msdn.microsoft.com/library/windows/desktop/ms724911) function used by this method does not explicitly handle strings which are NULL terminated. Both conditions should be checked for by the calling code.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CRegKey Class](../vs140/CRegKey-Class.md)   
 [CRegKey::SetMultiStringValue](../vs140/CRegKey--SetMultiStringValue.md)   
 [CRegKey::QueryBinaryValue](../vs140/CRegKey--QueryBinaryValue.md)   
 [CRegKey::QueryDWORDValue](../vs140/CRegKey--QueryDWORDValue.md)   
 [CRegKey::QueryGUIDValue](../vs140/CRegKey--QueryGUIDValue.md)   
 [CRegKey::QueryQWORDValue](../vs140/CRegKey--QueryQWORDValue.md)   
 [CRegKey::QueryStringValue](../vs140/CRegKey--QueryStringValue.md)