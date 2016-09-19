---
title: "CRowset::MoveNext"
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
ms.assetid: 0df3288c-2bce-494f-99c0-6344b54a4adf
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRowset::MoveNext
Moves the cursor to the next record.  
  
## Syntax  
  
```  
  
      HRESULT MoveNext( ) throw( );   
HRESULT MoveNext(   
   LONG lSkip,   
   bool bForward = true    
) throw( );  
```  
  
#### Parameters  
 `lSkip`  
 [in] The number of rows to skip before fetching.  
  
 `bForward`  
 [in] Pass **true** to move forward to the next record, **false** to move backward.  
  
## Return Value  
 A standard `HRESULT`. When the end of the rowset has been reached, returns **DB_S_ENDOFROWSET**.  
  
## Remarks  
 Fetches the next sequential row from the `CRowset` object, remembering the previous position. Optionally, you can choose to skip ahead `lSkip` rows or move backward.  
  
 This method requires that you set the following properties before calling **Open** on the table or command containing the rowset:  
  
-   **DBPROP_CANSCROLLBACKWARDS** must be `VARIANT_TRUE` if `lSkip` < 0  
  
-   **DBPROP_CANFETCHBACKWARDS** must be `VARIANT_TRUE` if `bForward` = false  
  
 Otherwise (if `lSkip` >= 0 and `bForward` = true), you do not need to set any additional properties.  
  
## Requirements  
 **Header:** atldbcli.h  
  
## See Also  
 [CRowset Class](../vs140/CRowset-Class.md)   
 [CRowset::MoveFirst](../vs140/CRowset--MoveFirst.md)   
 [CRowset::MoveToBookmark](../vs140/CRowset--MoveToBookmark.md)   
 [CRowset::MovePrev](../vs140/CRowset--MovePrev.md)   
 [CRowset::MoveLast](../vs140/CRowset--MoveLast.md)