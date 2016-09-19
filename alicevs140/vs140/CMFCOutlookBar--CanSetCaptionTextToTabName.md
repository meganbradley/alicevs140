---
title: "CMFCOutlookBar::CanSetCaptionTextToTabName"
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
ms.assetid: 31aa363f-b4da-4eb1-b386-59c28b34c99c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCOutlookBar::CanSetCaptionTextToTabName
Determines whether the caption for the tabbed pane displays the same text as the active tab.  
  
## Syntax  
  
```  
virtual BOOL CanSetCaptionTextToTabName() const;  
```  
  
## Return Value  
 `TRUE` if the Outlook bar window caption is automatically set to the text of the active tab; otherwise `FALSE`.  
  
## Remarks  
 Use [CBaseTabbedPane::EnableSetCaptionTextToTabName](../vs140/CBaseTabbedPane--EnableSetCaptionTextToTabName.md) to enable or disable this functionality.  
  
 In Outlook 2003 mode, this setting is always enabled.  
  
## Requirements  
 **Header:** afxoutlookbar.h  
  
## See Also  
 [CMFCOutlookBar Class](../vs140/CMFCOutlookBar-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)