---
title: "CRowset::MoveFirst"
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
ms.assetid: a17c0799-ead9-4d85-9a1d-8b17188d01e3
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRowset::MoveFirst
Moves the cursor to the initial position and retrieves the initial row.  
  
## Syntax  
  
```  
  
HRESULT MoveFirst( ) throw( );  
  
```  
  
## Return Value  
 A standard `HRESULT`.  
  
## Remarks  
 Calls [IRowset::RestartPosition](https://msdn.microsoft.com/en-us/library/ms712877.aspx) to reposition the next-fetch location to the initial position (the position that was the next-fetch location when the rowset was created) and retrieves the initial row.  
  
## Requirements  
 **Header:** atldbcli.h  
  
## See Also  
 [CRowset Class](../vs140/CRowset-Class.md)   
 [CRowset::MoveNext](../vs140/CRowset--MoveNext.md)   
 [CRowset::MoveToBookmark](../vs140/CRowset--MoveToBookmark.md)   
 [CRowset::MovePrev](../vs140/CRowset--MovePrev.md)   
 [CRowset::MoveLast](../vs140/CRowset--MoveLast.md)   
 [IRowset::RestartPosition](https://msdn.microsoft.com/en-us/library/ms712877.aspx)