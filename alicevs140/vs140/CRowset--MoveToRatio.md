---
title: "CRowset::MoveToRatio"
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
ms.assetid: 1fa313bd-8fd1-4608-8e85-44993b97dd88
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRowset::MoveToRatio
Fetches rows starting from a fractional position in the rowset.  
  
## Syntax  
  
```  
  
      HRESULT MoveToRatio(   
   DBCOUNTITEM nNumerator,   
   DBCOUNTITEM nDenominator,   
   bool bForward = true    
) throw( );  
```  
  
#### Parameters  
 `nNumerator`  
 [in] The numerator used to determine the fractional positional from which to fetch data.  
  
 `nDenominator`  
 [in] The denominator used to determine the fractional positional from which to fetch data.  
  
 `bForward`  
 [in] Indicates whether to move forward or backward. The default is forward.  
  
## Return Value  
 A standard `HRESULT`.  
  
## Remarks  
 `MoveToRatio` fetches rows according roughly to the following formula:  
  
 `( nNumerator *  RowsetSize ) / nDenominator`  
  
 where `RowsetSize` is the size of the rowset, measured in rows. The accuracy of this formula depends on the specific provider. For details, see [IRowsetScroll::GetRowsAtRatio](https://msdn.microsoft.com/en-us/library/ms709602.aspx).  
  
 This method requires the optional interface `IRowsetScroll`, which might not be supported on all providers; if this is the case, the method returns **E_NOINTERFACE**. You must also set **DBPROP_IRowsetScroll** to `VARIANT_TRUE` before calling **Open** on the table or command containing the rowset.  
  
## Requirements  
 **Header:** atldbcli.h  
  
## See Also  
 [CRowset Class](../vs140/CRowset-Class.md)