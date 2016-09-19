---
title: "CDynamicAccessor::AddBindEntry"
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
ms.assetid: 8f139376-7db3-4193-ba3b-63fe938ffa79
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDynamicAccessor::AddBindEntry
Adds a bind entry to the output columns.  
  
## Syntax  
  
```  
  
      HRESULT AddBindEntry(   
   const DBCOLUMNINFO& info    
) throw( );  
```  
  
#### Parameters  
 `info`  
 [in] A **DBCOLUMNINFO** structure containing column information. See "DBCOLUMNINFO Structures" in [IColumnsInfo::GetColumnInfo](https://msdn.microsoft.com/en-us/library/ms722704.aspx) in the *OLE DB Programmer's Reference*.  
  
## Return Value  
 One of the standard `HRESULT` values.  
  
## Remarks  
 Use this method when overriding the default accessor created with `CDynamicAccessor` (see [How Do I Fetch Data?](../vs140/Fetching-Data.md)).  
  
## Requirements  
 **Header:** atldbcli.h  
  
## See Also  
 [CDynamicAccessor Class](../vs140/CDynamicAccessor-Class.md)