---
title: "CRowset::Undo"
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
ms.assetid: 1ccd70e2-3931-41c4-893e-a05d0e295410
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRowset::Undo
Undoes any changes made to a row since the last fetch or [Update](../vs140/CRowset--Update.md).  
  
## Syntax  
  
```  
  
      HRESULT Undo(   
   DBCOUNTITEM* pcRows = NULL,   
   HROW* phRow = NULL,   
   DBROWSTATUS* pStatus = NULL    
) throw( );  
```  
  
#### Parameters  
 `pcRows`  
 [out] A pointer to the location where **Undo** returns the number of rows it attempted to undo if required.  
  
 `phRow`  
 [out] A pointer to the location where **Undo** returns an array of handles to all rows it attempted to undo if required.  
  
 `pStatus`  
 [out] A pointer to the location where **Undo** returns the row status value. No status is returned if `pStatus` is null.  
  
## Return Value  
 A standard `HRESULT`.  
  
## Remarks  
 This method requires the optional interface `IRowsetUpdate`, which might not be supported on all providers; if this is the case, the method returns **E_NOINTERFACE**. You must also set **DBPROP_IRowsetUpdate** to `VARIANT_TRUE` before calling **Open** on the table or command containing the rowset.  
  
## Requirements  
 **Header:** atldbcli.h  
  
## See Also  
 [CRowset Class](../vs140/CRowset-Class.md)   
 [IRowsetUpdate::Undo](https://msdn.microsoft.com/en-us/library/ms719655.aspx)