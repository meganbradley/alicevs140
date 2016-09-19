---
title: "COLUMN_ENTRY_TYPE"
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
ms.assetid: ac424261-ff6c-443b-a197-2cec8d78d738
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COLUMN_ENTRY_TYPE
Represents a binding to the specific column in the database. Supports `type` parameter.  
  
## Syntax  
  
```  
  
COLUMN_ENTRY_TYPE (  
nOrdinal  
,   
wType  
,   
data  
 )  
  
```  
  
#### Parameters  
 `nOrdinal`  
 [in] The column number.  
  
 `wType`  
 [in] Data type of column entry.  
  
 `data`  
 [in] The corresponding data member in the user record.  
  
## Remarks  
 This macro is a specialized variant of the [COLUMN_ENTRY](../vs140/COLUMN_ENTRY.md) macro that provides a means of specifying data type.  
  
## Requirements  
 **Header:** atldbcli.h  
  
## See Also  
 [Macros and Global Functions for OLE DB Consumer Templates](../vs140/Macros-and-Global-Functions-for-OLE-DB-Consumer-Templates.md)   
 [BEGIN_COLUMN_MAP](../vs140/BEGIN_COLUMN_MAP.md)   
 [END_COLUMN_MAP](../vs140/END_COLUMN_MAP.md)