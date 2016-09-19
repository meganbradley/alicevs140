---
title: "CMFCOutlookBarPane::GetRegularColor"
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
ms.assetid: 0cb74117-cd36-4373-932d-1b2dee7cac73
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCOutlookBarPane::GetRegularColor
Returns the regular (that is, non-selected) text color of the Outlook bar pane.  
  
## Syntax  
  
```  
DECLARE_MESSAGE_MAPCOLORREF GetRegularColor() const;  
```  
  
## Return Value  
 The current text color as an RGB color value.  
  
## Remarks  
 Use [CMFCOutlookBarPane::SetTextColor](../vs140/CMFCOutlookBarPane--SetTextColor.md) to set the current (regular and selected) text color of the Outlook bar. You can obtain the default text color by calling the [GetSysColor](http://msdn.microsoft.com/library/windows/desktop/ms724371) function with the `COLOR_WINDOW` index.  
  
## Requirements  
 **Header:** afxoutlookbarpane.h  
  
## See Also  
 [CMFCOutlookBarPane Class](../vs140/CMFCOutlookBarPane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)