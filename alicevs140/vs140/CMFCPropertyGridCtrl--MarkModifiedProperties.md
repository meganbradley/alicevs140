---
title: "CMFCPropertyGridCtrl::MarkModifiedProperties"
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
ms.assetid: 2e2e1c5f-5392-4ec8-9ec5-63e3481f6331
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPropertyGridCtrl::MarkModifiedProperties
Specifies how to display modified properties.  
  
## Syntax  
  
```  
void MarkModifiedProperties(  
   BOOL bMark=TRUE,  
   BOOL bRedraw=TRUE   
);  
```  
  
#### Parameters  
 [in] `bMark`  
 `TRUE` to display modified properties in bold style; `FALSE` to display modified properties in regular style. The default value is `TRUE`.  
  
 [in] `bRedraw`  
 `TRUE` to redraw the property grid control immediately; otherwise, `FALSE`. The default value is `TRUE`.  
  
## Remarks  
  
## Requirements  
 **Header:** afxpropertygridctrl.h  
  
## See Also  
 [CMFCPropertyGridCtrl Class](../vs140/CMFCPropertyGridCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)