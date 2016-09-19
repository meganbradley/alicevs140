---
title: "CMFCOutlookBar::GetButtonsFont"
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
ms.assetid: 8ebaf5ba-1c08-49a5-a984-5d92264cf950
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCOutlookBar::GetButtonsFont
Returns the font of the text on the page button tabs of the Outlook bar.  
  
## Syntax  
  
```  
CFont* GetButtonsFont() const;  
```  
  
## Return Value  
 A pointer to the font object that is used to display text on Outlook bar page button tabs.  
  
## Remarks  
 Use this function to retrieve the font that is used to display the text on Outlook page button tabs. You can set the font by calling on [CMFCOutlookBar::SetButtonsFont](../vs140/CMFCOutlookBar--SetButtonsFont.md).  
  
## Requirements  
 **Header:** afxoutlookbar.h  
  
## See Also  
 [CMFCOutlookBar Class](../vs140/CMFCOutlookBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFont](../vs140/CFont-Class.md)