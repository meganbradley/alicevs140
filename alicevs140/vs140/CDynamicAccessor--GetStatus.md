---
title: "CDynamicAccessor::GetStatus"
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
ms.assetid: 8f1aba69-5c2c-4ca7-ad84-7b4b27995eb8
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDynamicAccessor::GetStatus
Retrieves the status of the specified column.  
  
## Syntax  
  
```  
  
      bool GetStatus(   
   DBORDINAL nColumn,   
   DBSTATUS* pStatus    
) const throw( );  
bool GetStatus(  
   const CHAR* pColumnName,  
   DBSTATUS* pStatus   
) const throw( );  
bool GetStatus(  
   const WCHAR* pColumnName,  
   DBSTATUS* pStatus   
) const throw( );  
```  
  
#### Parameters  
 `nColumn`  
 [in] The column number. Column numbers start with 1. A value of 0 refers to the bookmark column, if any.  
  
 `pColumnName`  
 [in] A pointer to a character string containing the column name.  
  
 `pStatus`  
 [out] A pointer to the variable containing the column status. See [DBSTATUS](https://msdn.microsoft.com/en-us/library/ms722617.aspx) in the *OLE DB Programmer's Reference* for more information.  
  
## Return Value  
 Returns **true** if the specified column is found. Otherwise, this function returns **false**.  
  
## Requirements  
 **Header:** atldbcli.h  
  
## See Also  
 [CDynamicAccessor Class](../vs140/CDynamicAccessor-Class.md)   
 [CDynamicAccessor::SetStatus](../vs140/CDynamicAccessor--SetStatus.md)