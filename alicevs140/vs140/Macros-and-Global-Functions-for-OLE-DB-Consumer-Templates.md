---
title: "Macros and Global Functions for OLE DB Consumer Templates"
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
ms.assetid: 8765eb7b-32dd-407c-bacf-8890ef959837
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Macros and Global Functions for OLE DB Consumer Templates
The OLE DB Consumer Templates include the following macros and global functions:  
  
### Global Functions  
  
|||  
|-|-|  
|[AtlTraceErrorRecords](../vs140/AtlTraceErrorRecords.md)|Dumps OLE DB Error Record information to the dump device if an error is returned.|  
  
### Accessor Map Macros  
  
|||  
|-|-|  
|[BEGIN_ACCESSOR](../vs140/BEGIN_ACCESSOR.md)|Marks the beginning of an accessor entry.|  
|[BEGIN_ACCESSOR_MAP](../vs140/BEGIN_ACCESSOR_MAP.md)|Marks the beginning of the accessor map entries.|  
|[END_ACCESSOR](../vs140/END_ACCESSOR.md)|Marks the end of an accessor entry.|  
|[END_ACCESSOR_MAP](../vs140/END_ACCESSOR_MAP.md)|Marks the end of the accessor map entries.|  
  
### Column Map Macros  
  
|||  
|-|-|  
|[BEGIN_COLUMN_MAP](../vs140/BEGIN_COLUMN_MAP.md)|Marks the beginning of the column map entries in the user record class.|  
|[BLOB_ENTRY](../vs140/BLOB_ENTRY.md)|Used to bind a binary large object (BLOB).|  
|[BLOB_ENTRY_LENGTH](../vs140/BLOB_ENTRY_LENGTH.md)|Reports the length of the BLOB data column.|  
|[BLOB_ENTRY_LENGTH_STATUS](../vs140/BLOB_ENTRY_LENGTH_STATUS.md)|Reports the length and status of the BLOB data column.|  
|[BLOB_ENTRY_STATUS](../vs140/BLOB_ENTRY_STATUS.md)|Reports the status of the BLOB data column.|  
|[BLOB_NAME](../vs140/BLOB_NAME.md)|Used to bind a binary large object by column name.|  
|[BLOB_NAME_LENGTH](../vs140/BLOB_NAME_LENGTH.md)|Reports the length of the BLOB data column.|  
|[BLOB_NAME_LENGTH_STATUS](../vs140/BLOB_NAME_LENGTH_STATUS.md)|Reports the length and status of the BLOB data column.|  
|[BLOB_NAME_STATUS](../vs140/BLOB_NAME_STATUS.md)|Reports the status of the BLOB data column.|  
|[BOOKMARK_ENTRY](../vs140/BOOKMARK_ENTRY.md)|Represents a bookmark entry on the rowset. A bookmark entry is a special kind of column entry.|  
|[COLUMN_ENTRY](../vs140/COLUMN_ENTRY.md)|Represents a binding to a specific column in the database.|  
|[COLUMN_ENTRY_EX](../vs140/COLUMN_ENTRY_EX.md)|Represents a binding to the specific column in the database. Supports `type`, *length*, *precision*, `scale`, and *status* parameters.|  
|[COLUMN_ENTRY_LENGTH](../vs140/COLUMN_ENTRY_LENGTH.md)|Represents a binding to the specific column in the database. Supports the *length* variable.|  
|[COLUMN_ENTRY_LENGTH_STATUS](../vs140/COLUMN_ENTRY_LENGTH_STATUS.md)|Represents a binding to the specific column in the database. Supports *status* and *length* parameters.|  
|[COLUMN_ENTRY_PS](../vs140/COLUMN_ENTRY_PS.md)|Represents a binding to the specific column in the database. Supports *precision* and `scale` parameters.|  
|[COLUMN_ENTRY_PS_LENGTH](../vs140/COLUMN_ENTRY_PS_LENGTH.md)|Represents a binding to the specific column in the database. Supports the *length* variable, *precision* and `scale` parameters.|  
|[COLUMN_ENTRY_PS_LENGTH_STATUS](../vs140/COLUMN_ENTRY_PS_LENGTH_STATUS.md)|Represents a binding to the specific column in the database. Supports *status* and *length* variables, *precision* and `scale` parameters.|  
|[COLUMN_ENTRY_PS_STATUS](../vs140/COLUMN_ENTRY_PS_STATUS.md)|Represents a binding to the specific column in the database. Supports the *status* variable, *precision* and `scale` parameters.|  
|[COLUMN_ENTRY_STATUS](../vs140/COLUMN_ENTRY_STATUS.md)|Represents a binding to the specific column in the database. Supports the *status* variable.|  
|[COLUMN_ENTRY_TYPE](../vs140/COLUMN_ENTRY_TYPE.md)|Represents a binding to a specific column in the database. Supports `type` parameter.|  
|[COLUMN_ENTRY_TYPE_SIZE](../vs140/COLUMN_ENTRY_TYPE_SIZE.md)|Represents a binding to the specific column in the database. Supports `type` and `size` parameters.|  
|[COLUMN_NAME](../vs140/COLUMN_NAME.md)|Represents a binding to a specific column in the database by name.|  
|[COLUMN_NAME_EX](../vs140/COLUMN_NAME_EX.md)|Represents a binding to a specific column in the database by name. Supports specification of data type, size, precision, scale, column length, and column status.|  
|[COLUMN_NAME_LENGTH](../vs140/COLUMN_NAME_LENGTH.md)|Represents a binding to a specific column in the database by name. Supports specification of column length.|  
|[COLUMN_NAME_LENGTH_STATUS](../vs140/COLUMN_NAME_LENGTH_STATUS.md)|Represents a binding to a specific column in the database by name. Supports specification of column length and status.|  
|[COLUMN_NAME_PS](../vs140/COLUMN_NAME_PS.md)|Represents a binding to a specific column in the database by name. Supports specification of precision and scale.|  
|[COLUMN_NAME_PS_LENGTH](../vs140/COLUMN_NAME_PS_LENGTH.md)|Represents a binding to a specific column in the database by name. Supports specification of precision, scale, and column length.|  
|[COLUMN_NAME_PS_LENGTH_STATUS](../vs140/COLUMN_NAME_PS_LENGTH_STATUS.md)|Represents a binding to a specific column in the database by name. Supports specification of precision, scale, column length, and column status.|  
|[COLUMN_NAME_PS_STATUS](../vs140/COLUMN_NAME_PS_STATUS.md)|Represents a binding to a specific column in the database by name. Supports specification of precision, scale, and column status.|  
|[COLUMN_NAME_STATUS](../vs140/COLUMN_NAME_STATUS.md)|Represents a binding to a specific column in the database by name. Supports specification of column status.|  
|[COLUMN_NAME_TYPE](../vs140/COLUMN_NAME_TYPE.md)|Represents a binding to a specific column in the database by name. Supports specification of data type.|  
|[COLUMN_NAME_TYPE_PS](../vs140/COLUMN_NAME_TYPE_PS.md)|Represents a binding to a specific column in the database by name. Supports specification of data type, precision, and scale.|  
|[COLUMN_NAME_TYPE_SIZE](../vs140/COLUMN_NAME_TYPE_SIZE.md)|Represents a binding to a specific column in the database by name. Supports specification of data type and size.|  
|[COLUMN_NAME_TYPE_STATUS](../vs140/COLUMN_NAME_TYPE_STATUS.md)|Represents a binding to a specific column in the database by name. Supports specification of data type and column status.|  
|[END_COLUMN_MAP](../vs140/END_COLUMN_MAP.md)|Marks the end of the column map entries.|  
  
### Command Macros  
  
|||  
|-|-|  
|[DEFINE_COMMAND](../vs140/DEFINE_COMMAND.md)|Specifies the command that will be used to create the rowset when using the [CCommand](../vs140/CCommand-Class.md) class. Accepts only string types matching the specified application type (ANSI or Unicode). It is recommended that you use [DEFINE_COMMAND_EX](../vs140/DEFINE_COMMAND_EX.md) instead of `DEFINE_COMMAND`.|  
|[DEFINE_COMMAND_EX](../vs140/DEFINE_COMMAND_EX.md)|Specifies the command that will be used to create the rowset when using the [CCommand](../vs140/CCommand-Class.md) class. Supports ANSI and Unicode applications.|  
  
### Parameter Map Macros  
  
|||  
|-|-|  
|[BEGIN_PARAM_MAP](../vs140/BEGIN_PARAM_MAP.md)|Marks the beginning of the parameter map entries in the user record class.|  
|[END_PARAM_MAP](../vs140/END_PARAM_MAP.md)|Marks the end of the parameter map entries.|  
|[SET_PARAM_TYPE](../vs140/SET_PARAM_TYPE.md)|Specifies `COLUMN_ENTRY` macros that follow the `SET_PARAM_TYPE` macro as input, output, or input/output.|  
  
## See Also  
 [OLE DB Consumer Templates](../vs140/OLE-DB-Consumer-Templates--C---.md)   
 [OLE DB Consumer Templates](../vs140/OLE-DB-Consumer-Templates--C---.md)   
 [OLE DB Consumer Templates Reference](../vs140/OLE-DB-Consumer-Templates-Reference.md)