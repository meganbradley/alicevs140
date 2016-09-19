---
title: "IDBSchemaRowsetImpl::CheckRestrictions"
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
ms.assetid: 3c9d77d2-0e4b-48fa-80db-d735da19f1cf
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDBSchemaRowsetImpl::CheckRestrictions
Checks the validity of restrictions against a schema rowset.  
  
## Syntax  
  
```  
  
      HRESULT CheckRestrictions(  
   REFGUID rguidSchema,  
   ULONG cRestrictions,  
   const VARIANT rgRestrictions[]  
);  
```  
  
#### Parameters  
 `rguidSchema`  
 [in] A reference to the requested schema rowset GUID (for example, `DBSCHEMA_TABLES`).  
  
 `cRestrictions`  
 [in] The number of restrictions that the consumer passed in for the schema rowset.  
  
 `rgRestrictions`  
 [in] An array of length *cRestrictions* of restriction values to be set. For more information, see the description of the `rgRestrictions` parameter in [SetRestrictions](../vs140/IDBSchemaRowsetImpl--SetRestrictions.md).  
  
## Remarks  
 Use `CheckRestrictions` to check the validity of restrictions against a schema rowset. It checks restrictions for `DBSCHEMA_TABLES`, **DBSCHEMA_COLUMNS**, and **DBSCHEMA_PROVIDER_TYPES** schema rowsets. Call it to determine if a consumer's call to **IDBSchemaRowset::GetRowset** is correct. If you want to support schema rowsets other than those listed above, you should create your own function to carry out this task.  
  
 `CheckRestrictions` determines if the consumer is calling [GetRowset](../vs140/IDBSchemaRowsetImpl--GetRowset.md) with the correct restriction and the correct restriction type (for example, a `VT_BSTR` for a string) that the provider supports. It also determines if the correct number of restrictions are supported. By default, `CheckRestrictions` will ask the provider, through the [SetRestrictions](../vs140/IDBSchemaRowsetImpl--SetRestrictions.md) call, which restrictions it supports on a given rowset. It then compares the restrictions from the consumer against those supported by the provider and either succeeds or fails.  
  
 For more information on schema rowsets, see [IDBSchemaRowset](https://msdn.microsoft.com/en-us/library/ms713686.aspx) in the *OLE DB Programmer's Reference* in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atldb.h  
  
## See Also  
 [IDBSchemaRowsetImpl Class](../vs140/IDBSchemaRowsetImpl-Class.md)   
 [IDBSchemaRowsetImpl Class Members](assetId:///e74f6f82-541c-42e7-b4c6-e2d4656a0649)   
 [Schema Rowset Classes and Typedef Classes](../vs140/Schema-Rowset-Classes-and-Typedef-Classes.md)