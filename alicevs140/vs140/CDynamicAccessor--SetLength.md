---
title: "CDynamicAccessor::SetLength"
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
ms.topic: article
ms.assetid: 8109ae73-04ec-4a47-be97-ba1e60080384
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDynamicAccessor::SetLength
Sets the length of the specified column.  
  
## Syntax  
  
```  
  
      bool SetLength(   
   DBORDINAL nColumn,   
   DBLENGTH nLength    
) throw( );  
bool SetLength(   
   const CHAR* pColumnName,   
   DBLENGTH nLength    
) throw( );  
bool SetLength(   
   const WCHAR* pColumnName,   
   DBLENGTH nLength    
) throw( );  
```  
  
#### Parameters  
 `nColumn`  
 [in] The column number. Column numbers start with 1. A value of 0 refers to the bookmark column, if any.  
  
 `nLength`  
 [in] The length of the column in bytes.  
  
 `pColumnName`  
 [in] A pointer to a character string containing the column name.  
  
## Return Value  
 Returns **true** if the specified column length is set successfully. Otherwise, this function returns **false**.  
  
## Requirements  
 **Header:** atldbcli.h  
  
## See Also  
 [CDynamicAccessor Class](../vs140/CDynamicAccessor-Class.md)   
 [CDynamicAccessor::GetLength](../vs140/CDynamicAccessor--GetLength.md)