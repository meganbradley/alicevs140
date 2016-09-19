---
title: "CRegKey::QueryBinaryValue"
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
ms.assetid: 8ea8402c-8d26-47ac-aea7-2214192004ab
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRegKey::QueryBinaryValue
Call this method to retrieve the binary data for a specified value name.  
  
## Syntax  
  
```  
  
      LONG QueryBinaryValue(  
   LPCTSTR pszValueName,  
   void* pValue,  
   ULONG* pnBytes   
) throw( );  
```  
  
#### Parameters  
 `pszValueName`  
 Pointer to a null-terminated string containing the name of the value to query.  
  
 `pValue`  
 Pointer to a buffer that receives the value's data.  
  
 `pnBytes`  
 Pointer to a variable that specifies the size, in bytes, of the buffer pointed to by the `pValue` parameter. When the method returns, this variable contains the size of the data copied to the buffer.  
  
## Return Value  
 If the method succeeds, ERROR_SUCCESS is returned. If the method fails to read a value, it returns a nonzero error code defined in WINERROR.H. If the data referenced is not of type REG_BINARY, ERROR_INVALID_DATA is returned.  
  
## Remarks  
 This method makes use of **RegQueryValueEx** and confirms that the correct type of data is returned. See [RegQueryValueEx](http://msdn.microsoft.com/library/windows/desktop/ms724911) for more details.  
  
> [!IMPORTANT]
>  This method allows the caller to specify any registry location, potentially reading data which cannot be trusted. Also, the [RegQueryValueEx](http://msdn.microsoft.com/library/windows/desktop/ms724911) function used by this method does not explicitly handle strings which are NULL terminated. Both conditions should be checked for by the calling code.  
  
## See Also  
 [CRegKey Class](../vs140/CRegKey-Class.md)   
 [CRegKey::SetBinaryValue](../vs140/CRegKey--SetBinaryValue.md)   
 [CRegKey::QueryDWORDValue](../vs140/CRegKey--QueryDWORDValue.md)   
 [CRegKey::QueryGUIDValue](../vs140/CRegKey--QueryGUIDValue.md)   
 [CRegKey::QueryMultiStringValue](../vs140/CRegKey--QueryMultiStringValue.md)   
 [CRegKey::QueryQWORDValue](../vs140/CRegKey--QueryQWORDValue.md)   
 [CRegKey::QueryStringValue](../vs140/CRegKey--QueryStringValue.md)