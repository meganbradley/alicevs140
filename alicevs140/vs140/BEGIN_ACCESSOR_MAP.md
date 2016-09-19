---
title: "BEGIN_ACCESSOR_MAP"
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
ms.assetid: e6d6e3a4-62fa-4e49-8c53-caf8c9d20091
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# BEGIN_ACCESSOR_MAP
Marks the beginning of the accessor map entries.  
  
## Syntax  
  
```  
  
BEGIN_ACCESSOR_MAP(  
x  
,   
num  
 )  
  
```  
  
#### Parameters  
 *x*  
 [in] The name of the user record class.  
  
 *num*  
 [in] The number of accessors in this accessor map.  
  
## Remarks  
 In the case of multiple accessors on a rowset, you need to specify `BEGIN_ACCESSOR_MAP` at the beginning and use the `BEGIN_ACCESSOR` macro for each individual accessor. The `BEGIN_ACCESSOR` macro is completed with the `END_ACCESSOR` macro. The accessor map is completed with the `END_ACCESSOR_MAP` macro.  
  
 If you have only one accessor in the user record, use the macro [BEGIN_COLUMN_MAP](../vs140/BEGIN_COLUMN_MAP.md).  
  
## Example  
 [!CODE [NVC_OLEDB_Consumer#15](../CodeSnippet/VS_Snippets_Cpp/NVC_OLEDB_Consumer#15)]  
  
## Requirements  
 **Header:** atldbcli.h  
  
## See Also  
 [Macros and Global Functions for OLE DB Consumer Templates](../vs140/Macros-and-Global-Functions-for-OLE-DB-Consumer-Templates.md)   
 [BEGIN_ACCESSOR](../vs140/BEGIN_ACCESSOR.md)   
 [END_ACCESSOR](../vs140/END_ACCESSOR.md)   
 [END_ACCESSOR_MAP](../vs140/END_ACCESSOR_MAP.md)