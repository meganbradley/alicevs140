---
title: "CRowset::Delete"
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
ms.assetid: 4feb4f7e-139f-489a-b7d5-ea6ec0058e0f
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRowset::Delete
Calls [IRowsetChange::DeleteRows](https://msdn.microsoft.com/en-us/library/ms724362.aspx) to delete the current row from the rowset.  
  
## Syntax  
  
```  
  
HRESULT Delete( ) const throw( );  
  
```  
  
## Return Value  
 A standard `HRESULT`.  
  
## Requirements  
 **Header:** atldbcli.h  
  
## See Also  
 [CRowset Class](../vs140/CRowset-Class.md)