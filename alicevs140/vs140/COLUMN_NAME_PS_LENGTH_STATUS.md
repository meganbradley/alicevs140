---
title: "COLUMN_NAME_PS_LENGTH_STATUS"
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
ms.assetid: a1a2e2ca-f0ae-4896-8aa3-67a96c270b05
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COLUMN_NAME_PS_LENGTH_STATUS
Represents a binding on the rowset to the specific column in the rowset. Similar to [COLUMN_NAME](../vs140/COLUMN_NAME.md), except that this macro also takes precision, scale, column length, and column status.  
  
## Syntax  
  
```  
  
COLUMN_NAME_PS_LENGTH_STATUS(  
pszName  
,   
nPrecision  
,   
nScale  
,   
data  
,   
length  
,   
status )  
```  
  
#### Parameters  
 `pszName`  
 [in] A pointer to the column name. The name must be a Unicode string. You can accomplish this by putting an 'L' in front of the name, for example: `L"MyColumn"`.  
  
 `nPrecision`  
 [in] The maximum precision of the column you want to bind.  
  
 `nScale`  
 [in] The scale of the column you want to bind.  
  
 `data`  
 [in] The corresponding data member in the user record.  
  
 *length*  
 [in] The variable to be bound to the column length.  
  
 *status*  
 [in] The variable to be bound to the column status.  
  
## Remarks  
 See [COLUMN_NAME](../vs140/COLUMN_NAME.md) for information on where the **COLUMN_NAME_\*** macros are used.  
  
## Requirements  
 **Header:** atldbcli.h  
  
## See Also  
 [Macros and Global Functions for OLE DB Consumer Templates](../vs140/Macros-and-Global-Functions-for-OLE-DB-Consumer-Templates.md)   
 [BEGIN_ACCESSOR](../vs140/BEGIN_ACCESSOR.md)   
 [BEGIN_ACCESSOR_MAP](../vs140/BEGIN_ACCESSOR_MAP.md)   
 [BEGIN_COLUMN_MAP](../vs140/BEGIN_COLUMN_MAP.md)   
 [COLUMN_NAME](../vs140/COLUMN_NAME.md)   
 [COLUMN_NAME_EX](../vs140/COLUMN_NAME_EX.md)   
 [COLUMN_NAME_LENGTH](../vs140/COLUMN_NAME_LENGTH.md)   
 [COLUMN_NAME_LENGTH_STATUS](../vs140/COLUMN_NAME_LENGTH_STATUS.md)   
 [COLUMN_NAME_STATUS](../vs140/COLUMN_NAME_STATUS.md)   
 [COLUMN_NAME_PS](../vs140/COLUMN_NAME_PS.md)   
 [COLUMN_NAME_PS_LENGTH](../vs140/COLUMN_NAME_PS_LENGTH.md)   
 [COLUMN_NAME_PS_STATUS](../vs140/COLUMN_NAME_PS_STATUS.md)   
 [COLUMN_NAME_TYPE](../vs140/COLUMN_NAME_TYPE.md)   
 [COLUMN_NAME_TYPE_PS](../vs140/COLUMN_NAME_TYPE_PS.md)   
 [COLUMN_NAME_TYPE_SIZE](../vs140/COLUMN_NAME_TYPE_SIZE.md)   
 [COLUMN_NAME_TYPE_STATUS](../vs140/COLUMN_NAME_TYPE_STATUS.md)