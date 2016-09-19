---
title: "BLOB_ENTRY"
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
ms.assetid: 89e40678-0869-49ed-b502-0fa2630a9081
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# BLOB_ENTRY
Used with `BEGIN_COLUMN_MAP` and `END_COLUMN_MAP` to bind a binary large object ([BLOB](https://msdn.microsoft.com/en-us/library/ms711511.aspx)).  
  
## Syntax  
  
```  
  
BLOB_ENTRY(  
nOrdinal  
,  
 IID  
,   
flags  
,   
data  
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
  
## Example  
 See [How Can I Retrieve a BLOB?](../vs140/Retrieving-a-BLOB.md).  
  
## Requirements  
 **Header:** atldbcli.h  
  
## See Also  
 [Macros and Global Functions for OLE DB Consumer Templates](../vs140/Macros-and-Global-Functions-for-OLE-DB-Consumer-Templates.md)   
 [BEGIN_COLUMN_MAP](../vs140/BEGIN_COLUMN_MAP.md)   
 [END_COLUMN_MAP](../vs140/END_COLUMN_MAP.md)   
 [COLUMN_ENTRY](../vs140/COLUMN_ENTRY.md)   
 [BLOB_ENTRY_LENGTH](../vs140/BLOB_ENTRY_LENGTH.md)   
 [BLOB_ENTRY_LENGTH_STATUS](../vs140/BLOB_ENTRY_LENGTH_STATUS.md)   
 [BLOB_ENTRY_STATUS](../vs140/BLOB_ENTRY_STATUS.md)