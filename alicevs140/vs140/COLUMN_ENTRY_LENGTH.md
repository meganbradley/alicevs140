---
title: "COLUMN_ENTRY_LENGTH"
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
ms.assetid: 1758babf-204c-4d1d-b82a-f9a607072e9a
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COLUMN_ENTRY_LENGTH
Represents a binding on the rowset to the specific column in the database.  
  
## Syntax  
  
```  
  
COLUMN_ENTRY_LENGTH(  
nOrdinal  
,   
data  
,   
length  
 )  
  
```  
  
#### Parameters  
 See [DBBINDING](https://msdn.microsoft.com/en-us/library/ms716845.aspx) in the *OLE DB Programmer's Reference*.  
  
 `nOrdinal`  
 [in] The column number, starting with one. Bookmark corresponds to column zero.  
  
 `data`  
 [in] The corresponding data member in the user record.  
  
 *length*  
 [in] The variable to be bound to the column length.  
  
## Remarks  
 This macro supports the *length* variable. It is used in the following places:  
  
-   Between the [BEGIN_COLUMN_MAP](../vs140/BEGIN_COLUMN_MAP.md) and [END_COLUMN_MAP](../vs140/END_COLUMN_MAP.md) macros.  
  
-   Between the [BEGIN_ACCESSOR](../vs140/BEGIN_ACCESSOR.md) and [END_ACCESSOR](../vs140/END_ACCESSOR.md) macros.  
  
-   Between the [BEGIN_PARAM_MAP](../vs140/BEGIN_PARAM_MAP.md) and [END_PARAM_MAP](../vs140/END_PARAM_MAP.md) macros.  
  
## Requirements  
 **Header:** atldbcli.h  
  
## See Also  
 [Macros and Global Functions for OLE DB Consumer Templates](../vs140/Macros-and-Global-Functions-for-OLE-DB-Consumer-Templates.md)   
 [BEGIN_ACCESSOR](../vs140/BEGIN_ACCESSOR.md)   
 [BEGIN_ACCESSOR_MAP](../vs140/BEGIN_ACCESSOR_MAP.md)   
 [BEGIN_COLUMN_MAP](../vs140/BEGIN_COLUMN_MAP.md)   
 [COLUMN_ENTRY](../vs140/COLUMN_ENTRY.md)   
 [COLUMN_ENTRY_EX](../vs140/COLUMN_ENTRY_EX.md)   
 [COLUMN_ENTRY_PS](../vs140/COLUMN_ENTRY_PS.md)   
 [COLUMN_ENTRY_PS_LENGTH](../vs140/COLUMN_ENTRY_PS_LENGTH.md)   
 [COLUMN_ENTRY_LENGTH_STATUS](../vs140/COLUMN_ENTRY_LENGTH_STATUS.md)   
 [COLUMN_ENTRY_PS_LENGTH_STATUS](../vs140/COLUMN_ENTRY_PS_LENGTH_STATUS.md)   
 [COLUMN_ENTRY_STATUS](../vs140/COLUMN_ENTRY_STATUS.md)   
 [COLUMN_ENTRY_PS_STATUS](../vs140/COLUMN_ENTRY_PS_STATUS.md)   
 [END_ACCESSOR](../vs140/END_ACCESSOR.md)   
 [END_ACCESSOR_MAP](../vs140/END_ACCESSOR_MAP.md)   
 [END_COLUMN_MAP](../vs140/END_COLUMN_MAP.md)