---
title: "CDynamicAccessor::GetOrdinal"
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
ms.assetid: 2095b71c-a7a4-4034-89a1-77a78cb9633f
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDynamicAccessor::GetOrdinal
Retrieves the column number given a column name.  
  
## Syntax  
  
```  
  
      bool GetOrdinal(  
   const CHAR* pColumnName,  
   DBORDINAL* pOrdinal   
) const throw( );  
bool GetOrdinal(  
   const WCHAR* pColumnName,  
   DBORDINAL* pOrdinal   
) const throw( );  
```  
  
#### Parameters  
 `pColumnName`  
 [in] A pointer to a character string containing the column name.  
  
 *pOrdinal*  
 [out] A pointer to the column number.  
  
## Return Value  
 Returns **true** if a column with the specified name is found. Otherwise, this function returns **false**.  
  
## Requirements  
 **Header:** atldbcli.h  
  
## See Also  
 [CDynamicAccessor Class](../vs140/CDynamicAccessor-Class.md)