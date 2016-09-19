---
title: "SCHEMA_ENTRY"
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
ms.assetid: e8bee479-80f3-417e-8f41-cdaddd49690c
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# SCHEMA_ENTRY
Associates a GUID with a class.  
  
## Syntax  
  
```  
  
      SCHEMA_ENTRY(  
   guid,  
   rowsetClass   
);   
```  
  
#### Parameters  
 `guid`  
 A schema rowset GUID. See [IDBSchemaRowset](https://msdn.microsoft.com/en-us/library/ms713686.aspx) in the *OLE DB Programmer's Reference* for a list of schema rowsets and their GUIDs.  
  
 *rowsetClass*  
 The class that will be created to represent the schema rowset.  
  
## Remarks  
 [IDBSchemaRowsetImpl](../vs140/IDBSchemaRowsetImpl-Class.md) can then query the map for a list of GUIDs, or it can create a rowset if it is given a GUID. The schema rowset `IDBSchemaRowsetImpl` creates is similar to a standard `CRowsetImpl`-derived class, except it must provide an **Execute** method that has the following signature:  
  
 `HRESULT Execute (LONG* pcRowsAffected, ULONG cRestrictions,`  
  
 `const VARIANT* rgRestrictions)`  
  
 This **Execute** function populates the rowset's data. The ATL Project Wizard creates, as described in [IDBSchemaRowset](https://msdn.microsoft.com/en-us/library/ms713686.aspx) in the *OLE DB Programmer's Reference*, three initial schema rowsets in the project for each of the three mandatory OLE DB schemas:  
  
-   `DBSCHEMA_TABLES`  
  
-   **DBSCHEMA_COLUMNS**  
  
-   **DBSCHEMA_PROVIDER_TYPES**  
  
 The wizard also adds three corresponding entries in the schema map. See [Creating an OLE DB Template Provider](../vs140/Creating-an-OLE-DB-Provider.md) for more information about using the wizard to create a provider.  
  
## Requirements  
 **Header:** atldb.h  
  
## See Also  
 [Macros for OLE DB Provider Templates](../vs140/Macros-for-OLE-DB-Provider-Templates.md)   
 [BEGIN_SCHEMA_MAP](../vs140/BEGIN_SCHEMA_MAP.md)   
 [END_SCHEMA_MAP](../vs140/END_SCHEMA_MAP.md)