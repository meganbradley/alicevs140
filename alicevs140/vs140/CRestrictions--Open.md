---
title: "CRestrictions::Open"
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
ms.assetid: 0aff0cc3-543a-47d2-8d6b-ebb36926b6db
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRestrictions::Open
Returns a result set according to the user-supplied restrictions.  
  
## Syntax  
  
```  
  
      HRESULT Open(  
   const CSession& session,  
   LPCTSTR lpszParam 1 = NULL,  
   LPCTSTR lpszParam 2 = NULL,  
   LPCTSTR lpszParam 3 = NULL,  
   LPCTSTR lpszParam 4 = NULL,  
   LPCTSTR lpszParam 5 = NULL,  
   LPCTSTR lpszParam 6 = NULL,  
   LPCTSTR lpszParam 7 = NULL,  
   bool bBind = true  
);  
```  
  
#### Parameters  
 `session`  
 [in] Specifies an existing session object used to connect to the data source.  
  
 *lpszParam*  
 [in] Specifies the restrictions on the schema rowset.  
  
 `bBind`  
 [in] Specifies whether to bind the column map automatically. The default is **true**, which causes the column map to be bound automatically. Setting `bBind` to **false** prevents the automatic binding of the column map so that you can bind manually. (Manual binding is of particular interest to OLAP users.)  
  
## Return Value  
 One of the standard `HRESULT` values.  
  
## Remarks  
 You can specify a maximum of seven restrictions on a schema rowset.  
  
 See [IDBSchemaRowset](https://msdn.microsoft.com/en-us/library/ms713686.aspx) for information about the defined restrictions on each schema rowset.  
  
## Requirements  
 **Header:** atldbsch.h  
  
## See Also  
 [CRestrictions Class](../vs140/CRestrictions-Class.md)   
 [Schema Rowset Classes and Typedef Classes](../vs140/Schema-Rowset-Classes-and-Typedef-Classes.md)