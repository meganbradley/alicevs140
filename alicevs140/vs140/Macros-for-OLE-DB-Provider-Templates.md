---
title: "Macros for OLE DB Provider Templates"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 909482c5-64ab-4e52-84a9-1c07091db183
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Macros for OLE DB Provider Templates
The OLE DB Templates Provider macros offer functionality in the following categories:  
  
### Property Set Map Macros  
  
|||  
|-|-|  
|[BEGIN_PROPERTY_SET](../vs140/BEGIN_PROPERTY_SET.md)|Marks the beginning of a property set.|  
|[BEGIN_PROPERTY_SET_EX](../vs140/BEGIN_PROPERTY_SET_EX.md)|Marks the beginning of a property set.|  
|[BEGIN_PROPSET_MAP](../vs140/BEGIN_PROPSET_MAP.md)|Marks the beginning of a property set that can be hidden or defined outside the scope of the provider.|  
|[CHAIN_PROPERTY_SET](../vs140/CHAIN_PROPERTY_SET.md)|Chains property groups together.|  
|[END_PROPERTY_SET](../vs140/END_PROPERTY_SET.md)|Marks the end of a property set.|  
|[END_PROPSET_MAP](../vs140/END_PROPSET_MAP.md)|Marks the end of a property set map.|  
|[PROPERTY_INFO_ENTRY](../vs140/PROPERTY_INFO_ENTRY.md)|Sets a specific property in a property set to a default value.|  
|[PROPERTY_INFO_ENTRY_EX](../vs140/PROPERTY_INFO_ENTRY_EX.md)|Sets a specific property in a property set to a value supplied by you. Also enables you to set flags and options.|  
|[PROPERTY_INFO_ENTRY_VALUE](../vs140/PROPERTY_INFO_ENTRY_VALUE.md)|Sets a specific property in a property set to a value supplied by you.|  
  
### Column Map Macros  
  
|||  
|-|-|  
|[BEGIN_PROVIDER_COLUMN_MAP](../vs140/BEGIN_PROVIDER_COLUMN_MAP.md)|Marks the beginning of the provider column map entries.|  
|[END_PROVIDER_COLUMN_MAP](../vs140/END_PROVIDER_COLUMN_MAP.md)|Marks the end of the provider column map entries.|  
|[PROVIDER_COLUMN_ENTRY](../vs140/PROVIDER_COLUMN_ENTRY.md)|Represents a specific column supported by the provider.|  
|[PROVIDER_COLUMN_ENTRY_GN](../vs140/PROVIDER_COLUMN_ENTRY_GN.md)|Represents a specific column supported by the provider. You can specify the column's size, data type, precision, scale, and schema rowset GUID.|  
|[PROVIDER_COLUMN_ENTRY_FIXED](../vs140/PROVIDER_COLUMN_ENTRY_FIXED.md)|Represents a specific column supported by the provider. You can specify the column data type.|  
|[PROVIDER_COLUMN_ENTRY_LENGTH](../vs140/PROVIDER_COLUMN_ENTRY_LENGTH.md)|Represents a specific column supported by the provider. You can specify the column size.|  
|[PROVIDER_COLUMN_ENTRY_STR](../vs140/PROVIDER_COLUMN_ENTRY_STR.md)|Represents a specific column supported by the provider. It assumes the column type is a string.|  
|[PROVIDER_COLUMN_ENTRY_TYPE_LENGTH](../vs140/PROVIDER_COLUMN_ENTRY_TYPE_LENGTH.md)|Represents a specific column supported by the provider. Like PROVIDER_COLUMN_ENTRY_LENGTH, but also allows you to specify the column's data type as well as size.|  
|[PROVIDER_COLUMN_ENTRY_WSTR](../vs140/PROVIDER_COLUMN_ENTRY_WSTR.md)|Represents a specific column supported by the provider. It assumes the column type is a Unicode character string.|  
  
### Schema Rowset Macros  
  
|||  
|-|-|  
|[BEGIN_SCHEMA_MAP](../vs140/BEGIN_SCHEMA_MAP.md)|Marks the beginning of a schema map.|  
|[SCHEMA_ENTRY](../vs140/SCHEMA_ENTRY.md)|Associates a GUID with a class.|  
|[END_SCHEMA_MAP](../vs140/END_SCHEMA_MAP.md)|Marks the end of a schema map.|  
  
## See Also  
 [OLE DB Provider Templates](../vs140/OLE-DB-Provider-Templates--C---.md)   
 [OLE DB Provider Template Architecture](../vs140/OLE-DB-Provider-Template-Architecture.md)   
 [Creating an OLE DB Provider](../vs140/Creating-an-OLE-DB-Provider.md)   
 [OLE DB Provider Templates Reference](../vs140/OLE-DB-Provider-Templates-Reference.md)