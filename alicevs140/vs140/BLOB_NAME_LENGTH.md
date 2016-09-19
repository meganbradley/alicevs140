---
title: "BLOB_NAME_LENGTH"
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
ms.assetid: 38150260-a127-486d-a7ab-0d01b731b6fd
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# BLOB_NAME_LENGTH
Used with `BEGIN_COLUMN_MAP` and `END_COLUMN_MAP` to bind a binary large object ([BLOB](https://msdn.microsoft.com/en-us/library/ms711511.aspx)). Similar to [BLOB_NAME](../vs140/BLOB_NAME.md), except that this macro also gets the length in bytes of the BLOB data column.  
  
## Syntax  
  
```  
  
BLOB_NAME_LENGTH(  
pszName  
,   
IID  
,   
flags  
,   
data  
,   
length )  
```  
  
#### Parameters  
 `pszName`  
 [in] A pointer to the column name. The name must be a Unicode string. You can accomplish this by putting an 'L' in front of the name, for example: `L"MyColumn"`.  
  
 *IID*  
 [in] Interface GUID, such as **IDD_ISequentialStream**, used to retrieve the BLOB.  
  
 `flags`  
 [in] Storage-mode flags as defined by the OLE Structured Storage model (for example, **STGM_READ**).  
  
 `data`  
 [in] The corresponding data member in the user record.  
  
 *length*  
 [out] The (actual) length in bytes of the BLOB column.  
  
## Requirements  
 **Header:** atldbcli.h  
  
## See Also  
 [Macros and Global Functions for OLE DB Consumer Templates](../vs140/Macros-and-Global-Functions-for-OLE-DB-Consumer-Templates.md)   
 [BEGIN_COLUMN_MAP](../vs140/BEGIN_COLUMN_MAP.md)   
 [END_COLUMN_MAP](../vs140/END_COLUMN_MAP.md)   
 [COLUMN_ENTRY](../vs140/COLUMN_ENTRY.md)   
 [BLOB_NAME](../vs140/BLOB_NAME.md)   
 [BLOB_NAME_LENGTH_STATUS](../vs140/BLOB_NAME_LENGTH_STATUS.md)   
 [BLOB_NAME_STATUS](../vs140/BLOB_NAME_STATUS.md)