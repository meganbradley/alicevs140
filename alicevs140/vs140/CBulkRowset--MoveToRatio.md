---
title: "CBulkRowset::MoveToRatio"
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
ms.assetid: 86be60f5-9341-44c1-8e1e-9174c082d0d5
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBulkRowset::MoveToRatio
Fetches rows starting from a fractional position in the rowset.  
  
## Syntax  
  
```  
  
      HRESULT MoveToRatio(  
   DBCOUNTITEM nNumerator,  
   DBCOUNTITEM nDenominator   
) throw( );  
```  
  
#### Parameters  
 `nNumerator`  
 [in] The numerator used to determine the fractional position from which to fetch data.  
  
 `nDenominator`  
 [in] The denominator used to determine the fractional position from which to fetch data.  
  
## Return Value  
 A standard `HRESULT`.  
  
## Remarks  
 `MoveToRatio` fetches the rows roughly according to the following formula:  
  
 `( nNumerator *  RowsetSize ) / nDenominator`  
  
 Where `RowsetSize` is the size of the rowset, measured in rows. The accuracy of this formula depends on the specific provider. For details, see [IRowsetScroll::GetRowsAtRatio](https://msdn.microsoft.com/en-us/library/ms709602.aspx) in the *OLE DB Programmer's Reference*.  
  
## Requirements  
 **Header:** atldbcli.h  
  
## See Also  
 [CBulkRowset Class](../vs140/CBulkRowset-Class.md)