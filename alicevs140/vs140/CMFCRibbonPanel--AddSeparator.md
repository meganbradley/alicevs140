---
title: "CMFCRibbonPanel::AddSeparator"
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
ms.assetid: a312e0e6-522d-46bd-b9cd-8e61edbde3ce
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonPanel::AddSeparator
Adds a separator to the ribbon panel.  
  
## Syntax  
  
```  
virtual void AddSeparator();  
```  
  
## Remarks  
 Call this method to add a separator to the ribbon panel. The separator will be added next to the ribbon element that was added by the previous call to [CMFCRibbonPanel::Add](../vs140/CMFCRibbonPanel--Add.md). To insert a separator at a given position, call [CMFCRibbonPanel::InsertSeparator](../vs140/CMFCRibbonPanel--InsertSeparator.md).  
  
## Requirements  
 **Header:** afxRibbonPanel.h  
  
## See Also  
 [CMFCRibbonPanel Class](../vs140/CMFCRibbonPanel-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)