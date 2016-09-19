---
title: "BLOB_ENTRY_LENGTH"
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
ms.assetid: 832d21ab-5fdd-49ad-af6e-4fca5722ec93
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# BLOB_ENTRY_LENGTH
Used with `BEGIN_COLUMN_MAP` and `END_COLUMN_MAP` to bind a binary large object ([BLOB](https://msdn.microsoft.com/en-us/library/ms711511.aspx)). Similar to [BLOB_ENTRY](../vs140/BLOB_ENTRY.md), except that this macro also gets the length in bytes of the BLOB column.  
  
## Syntax  
  
```  
  
BLOB_ENTRY_LENGTH(  
nOrdinal  
,   
IID  
,   
flags  
,   
data  
,   
length  
 )  
  
```  
  
#### Parameters  
 `nOrdinal`  
 [in] The column number.  
  
 *IID*  
 [in] Interface GUID, such as **IDD_ISequentialStream**, used to retrieve the BLOB.  
  
 `flags`  
 [in] Storage-mode flags as defined by the OLE Structured Storage model (for example, **STGM_READ**).  
  
 `data`  
 [in] The corresponding data member in the user record.  
  
 *length*  
 [out] The (actual) length in bytes of the BLOB column.  
  
## Example  
 See [How Can I Retrieve a BLOB?](../vs140/Retrieving-a-BLOB.md).  
  
## Requirements  
 **Header:** atldbcli.h  
  
## See Also  
 [Macros and Global Functions for OLE DB Consumer Templates](../vs140/Macros-and-Global-Functions-for-OLE-DB-Consumer-Templates.md)   
 [BEGIN_COLUMN_MAP](../vs140/BEGIN_COLUMN_MAP.md)   
 [END_COLUMN_MAP](../vs140/END_COLUMN_MAP.md)   
 [COLUMN_ENTRY](../vs140/COLUMN_ENTRY.md)   
 [BLOB_ENTRY](../vs140/BLOB_ENTRY.md)   
 [BLOB_ENTRY_LENGTH_STATUS](../vs140/BLOB_ENTRY_LENGTH_STATUS.md)   
 [BLOB_ENTRY_STATUS](../vs140/BLOB_ENTRY_STATUS.md)