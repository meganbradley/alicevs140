---
title: "CRowset::Update"
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
ms.assetid: cd5fedc8-2b85-4cb8-8c40-c79576316903
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRowset::Update
Transmits any pending changes made to the current row since the last fetch or **Update** call on it.  
  
## Syntax  
  
```  
  
      HRESULT Update(   
   DBCOUNTITEM* pcRows = NULL,   
   HROW* phRow = NULL,   
   DBROWSTATUS* pStatus = NULL    
) throw( );  
```  
  
#### Parameters  
 `pcRows`  
 [out] A pointer to the location where **Update** returns the number of rows it attempted to update, if required.  
  
 `phRow`  
 [out] A pointer to the location where **Update** returns the handle of the row it attempted to update. No handle is returned if `phRow` is null.  
  
 `pStatus`  
 [out] A pointer to the location where **Update** returns the row status value. No status is returned if `pStatus` is null.  
  
## Return Value  
 A standard `HRESULT`.  
  
## Remarks  
 Transmits any pending changes made to the current row since that row was last fetched or updated (using **Update** or [UpdateAll](../vs140/CRowset--UpdateAll.md)). You typically call [SetData](../vs140/CRowset--SetData.md) to set data values in columns in a row, and then call **Update** to transmit those changes.  
  
 This method requires the optional interface `IRowsetUpdate`, which might not be supported on all providers; if this is the case, the method returns **E_NOINTERFACE**. You must also set **DBPROP_IRowsetUpdate** to `VARIANT_TRUE` before calling **Open** on the table or command containing the rowset.  
  
## Requirements  
 **Header:** atldbcli.h  
  
## See Also  
 [CRowset Class](../vs140/CRowset-Class.md)   
 [IRowsetUpdate::Update](https://msdn.microsoft.com/en-us/library/ms719709.aspx)   
 [CRowset::UpdateAll](../vs140/CRowset--UpdateAll.md)   
 [CRowset::SetData](../vs140/CRowset--SetData.md)