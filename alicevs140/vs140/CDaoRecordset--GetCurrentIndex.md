---
title: "CDaoRecordset::GetCurrentIndex"
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
ms.topic: reference
ms.assetid: 4980bee1-426e-4131-ac23-afa2c9cad4ce
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoRecordset::GetCurrentIndex
Call this member function to determine the index currently in use in an indexed table-type `CDaoRecordset` object.  
  
## Syntax  
  
```  
  
CString GetCurrentIndex( );  
  
```  
  
## Return Value  
 A `CString` containing the name of the index currently in use with a table-type recordset. Returns an empty string if no index has been set.  
  
## Remarks  
 This index is the basis for ordering records in a table-type recordset, and is used by the [Seek](../vs140/CDaoRecordset--Seek.md) member function to locate records.  
  
 A `CDaoRecordset` object can have more than one index but can use only one index at a time (although a [CDaoTableDef](../vs140/CDaoTableDef-Class.md) object may have several indexes defined on it).  
  
 For related information, see the topic "Index Object" and the definition "current index" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoRecordset Class](../vs140/CDaoRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoRecordset::SetCurrentIndex](../vs140/CDaoRecordset--SetCurrentIndex.md)