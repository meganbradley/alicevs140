---
title: "CBulkRowset::AddRefRows"
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
ms.assetid: 014be991-50f8-4377-ba16-fec80b54b406
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBulkRowset::AddRefRows
Calls [IRowset::AddRefRows](https://msdn.microsoft.com/en-us/library/ms719619.aspx) to increment the reference count for all rows currently retrieved from the bulk rowset.  
  
## Syntax  
  
```  
  
HRESULT AddRefRows( ) throw( );  
  
```  
  
## Return Value  
 A standard `HRESULT`.  
  
## Requirements  
 **Header:** atldbcli.h  
  
## See Also  
 [CBulkRowset Class](../vs140/CBulkRowset-Class.md)   
 [CBulkRowset::ReleaseRows](../vs140/CBulkRowset--ReleaseRows.md)