---
title: "CMFCRibbonPanel::InsertSeparator"
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
ms.assetid: 7170fe91-b132-47a5-b032-b3106e94ec41
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonPanel::InsertSeparator
Inserts a separator at the given position.  
  
## Syntax  
  
```  
virtual BOOL InsertSeparator(  
    int nIndex  
);  
```  
  
#### Parameters  
 [in] `nIndex`  
 Specifies the zero-based index where the separator is inserted.  
  
## Return Value  
 `TRUE` if the separator has been inserted successfully; otherwise, `FALSE`.  
  
## Remarks  
 Call this method to insert a separator at the position specified by `nIndex`. To insert a separator next to the most recently added ribbon element, call [CMFCRibbonPanel::AddSeparator](../vs140/CMFCRibbonPanel--AddSeparator.md).  
  
## Requirements  
 **Header:** afxRibbonPanel.h  
  
## See Also  
 [CMFCRibbonPanel Class](../vs140/CMFCRibbonPanel-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)