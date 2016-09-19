---
title: "IDBSchemaRowsetImpl::CreateSchemaRowset"
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
ms.assetid: ad3e3e4d-45b9-461c-b7b8-3af6843631b1
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDBSchemaRowsetImpl::CreateSchemaRowset
Implements a COM object creator function for the object specified by the template parameter.  
  
## Syntax  
  
```  
  
      template < class   
      SchemaRowsetClass  
       >  
HRESULT CreateSchemaRowset(  
   IUnknown *pUnkOuter,  
   ULONG cRestrictions,  
   const VARIANT rgRestrictions[],  
   REFIID riid,  
   ULONG cPropertySets,  
   DBPROPSET rgPropertySets[],  
   IUnknown** ppRowset,  
   SchemaRowsetClass*& pSchemaRowset   
);  
```  
  
#### Parameters  
 `pUnkOuter`  
 [in] An outer [IUnknown](http://msdn.microsoft.com/library/windows/desktop/ms680509) when aggregating, otherwise **NULL**.  
  
 `cRestrictions`  
 [in] The count of restrictions applied to the schema rowset.  
  
 `rgRestrictions`  
 [in] An array of `cRestrictions`**VARIANT**s to be applied to the rowset.  
  
 `riid`  
 [in] The interface to [QueryInterface](../vs140/QueryInterface.md) for on the output **IUnknown**.  
  
 `cPropertySets`  
 [in] The number of property sets to set.  
  
 `rgPropertySets`  
 [in] An array of [DBPROPSET](https://msdn.microsoft.com/en-us/library/ms714367.aspx) structures that specify the properties being set.  
  
 `ppRowset`  
 [out] The outgoing **IUnknown** requested by `riid`. This **IUnknown** is an interface on the schema rowset object.  
  
 `pSchemaRowset`  
 [out] A pointer to an instance of the schema rowset class. Typically, this parameter is not used, but it can be used if you must perform more work on the schema rowset before handing it out to a COM object. The lifetime of `pSchemaRowset` is bound by `ppRowset`.  
  
## Return Value  
 A standard `HRESULT` value.  
  
## Remarks  
 This function implements a generic creator for all types of schema rowsets. Typically, the user does not call this function. It is called by the implementation of the schema map.  
  
## Requirements  
 **Header:** atldb.h  
  
## See Also  
 [IDBSchemaRowsetImpl Class](../vs140/IDBSchemaRowsetImpl-Class.md)   
 [IDBSchemaRowsetImpl Class Members](assetId:///e74f6f82-541c-42e7-b4c6-e2d4656a0649)   
 [SCHEMA_ENTRY](../vs140/SCHEMA_ENTRY.md)   
 [Schema Rowset Classes and Typedef Classes](../vs140/Schema-Rowset-Classes-and-Typedef-Classes.md)