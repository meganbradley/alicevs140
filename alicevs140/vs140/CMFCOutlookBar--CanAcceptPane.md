---
title: "CMFCOutlookBar::CanAcceptPane"
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
ms.assetid: da87e1cb-e10f-4039-9e2f-4324f3a687b1
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCOutlookBar::CanAcceptPane
Determines whether another pane can be docked to the Outlook bar pane.  
  
## Syntax  
  
```  
virtual BOOL CanAcceptPane(  
   const CBasePane* pBar  
) const;  
```  
  
#### Parameters  
 [in] `pBar`  
 A pointer to another pane that is being docked to this pane.  
  
## Return Value  
 `TRUE` if another pane can be docked to the Outlook bar pane; otherwise `FALSE`.  
  
## Remarks  
 If the Outlook bar is in Outlook 2003 mode, docking is not supported, so the return value is `FALSE`.  
  
 If the `pBar` parameter is `NULL`, this method returns `FALSE`.  
  
 Otherwise, this method behaves as the base method [CBasePane::CanAcceptPane](../vs140/CBasePane--CanAcceptPane.md), except that even if docking is not enabled, an Outlook bar can still enable another Outlook bar to be docked over it.  
  
## Requirements  
 **Header:** afxoutlookbar.h  
  
## See Also  
 [CMFCOutlookBar Class](../vs140/CMFCOutlookBar-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)