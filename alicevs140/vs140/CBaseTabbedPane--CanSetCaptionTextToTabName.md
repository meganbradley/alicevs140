---
title: "CBaseTabbedPane::CanSetCaptionTextToTabName"
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
ms.assetid: b7d2f7f6-7be5-44c3-807b-ab3706c610cc
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBaseTabbedPane::CanSetCaptionTextToTabName
Determines whether the caption for the tabbed pane should display the same text as the active tab.  
  
## Syntax  
  
```  
virtual BOOL CanSetCaptionTextToTabName() const;  
```  
  
## Return Value  
 `TRUE` if the caption text of the tabbed pane is set to the text of the active tab; otherwise, `FALSE`.  
  
## Remarks  
 The method is used to determine whether the text displayed on the tabbed pane caption duplicates the label of the active tab. You can enable or disable this functionality by calling [CBaseTabbedPane::EnableSetCaptionTextToTabName](../vs140/CBaseTabbedPane--EnableSetCaptionTextToTabName.md).  
  
## Requirements  
 **Header:** afxBaseTabbedPane.h  
  
## See Also  
 [CBaseTabbedPane Class](../vs140/CBaseTabbedPane-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)