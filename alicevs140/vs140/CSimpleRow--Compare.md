---
title: "CSimpleRow::Compare"
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
ms.assetid: 0bb65f09-c7bc-449b-aa4e-c828cac13510
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSimpleRow::Compare
Compares two rows to see if they refer to the same row instance.  
  
## Syntax  
  
```  
  
      HRESULT Compare(   
   CSimpleRow* pRow    
);  
```  
  
#### Parameters  
 `pRow`  
 A pointer to a `CSimpleRow` object.  
  
## Return Value  
 An `HRESULT` value, usually `S_OK`, indicating the two rows are the same row instance, or **S_FALSE**, indicating the two rows are different. See [IRowsetIdentity::IsSameRow](https://msdn.microsoft.com/en-us/library/ms719629.aspx) in the *OLE DB Programmer's Reference* for other possible return values.  
  
## Requirements  
 **Header:** atldb.h  
  
## See Also  
 [CSimpleRow Class](../vs140/CSimpleRow-Class.md)   
 [CSimpleRow::ReleaseRow](../vs140/CSimpleRow--ReleaseRow.md)   
 [IRowsetImpl::RefRows](../vs140/IRowsetImpl--RefRows.md)