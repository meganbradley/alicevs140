---
title: "CBulkRowset::SetRows"
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
ms.assetid: 7e92312a-bfd0-4c24-a799-62bef663f28e
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBulkRowset::SetRows
Sets the number of row handles retrieved by each call.  
  
## Syntax  
  
```  
  
      void SetRows(  
   DBROWCOUNT nRows   
) throw( );  
```  
  
#### Parameters  
 `nRows`  
 [in] The new size of the rowset (number of rows).  
  
## Remarks  
 If you call this function, it must be before the rowset is opened.  
  
## Requirements  
 **Header:** atldbcli.h  
  
## See Also  
 [CBulkRowset Class](../vs140/CBulkRowset-Class.md)