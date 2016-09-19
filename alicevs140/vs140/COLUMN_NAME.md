---
title: "COLUMN_NAME"
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
ms.assetid: a213b9a0-2148-4a08-9111-d9fa8fdec462
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COLUMN_NAME
Represents a binding on the rowset to the specific column in the rowset. Similar to [COLUMN_ENTRY](../vs140/COLUMN_ENTRY.md), except that this macro takes the column name instead of the column number.  
  
## Syntax  
  
```  
  
COLUMN_NAME(  
pszName  
,   
data  
 )  
  
```  
  
#### Parameters  
 `pszName`  
 [in] A pointer to the column name. The name must be a Unicode string. You can accomplish this by putting an 'L' in front of the name, for example: `L"MyColumn"`.  
  
 `data`  
 [in] The corresponding data member in the user record.  
  
## Remarks  
 The **COLUMN_NAME_\*** macros are used in the same places as [COLUMN_ENTRY](../vs140/COLUMN_ENTRY.md):  
  
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
 [COLUMN_NAME_EX](../vs140/COLUMN_NAME_EX.md)   
 [COLUMN_NAME_LENGTH](../vs140/COLUMN_NAME_LENGTH.md)   
 [COLUMN_NAME_LENGTH_STATUS](../vs140/COLUMN_NAME_LENGTH_STATUS.md)   
 [COLUMN_NAME_STATUS](../vs140/COLUMN_NAME_STATUS.md)   
 [COLUMN_NAME_PS](../vs140/COLUMN_NAME_PS.md)   
 [COLUMN_NAME_PS_LENGTH](../vs140/COLUMN_NAME_PS_LENGTH.md)   
 [COLUMN_NAME_PS_STATUS](../vs140/COLUMN_NAME_PS_STATUS.md)   
 [COLUMN_NAME_PS_LENGTH_STATUS](../vs140/COLUMN_NAME_PS_LENGTH_STATUS.md)   
 [COLUMN_NAME_TYPE](../vs140/COLUMN_NAME_TYPE.md)   
 [COLUMN_NAME_TYPE_PS](../vs140/COLUMN_NAME_TYPE_PS.md)   
 [COLUMN_NAME_TYPE_SIZE](../vs140/COLUMN_NAME_TYPE_SIZE.md)   
 [COLUMN_NAME_TYPE_STATUS](../vs140/COLUMN_NAME_TYPE_STATUS.md)