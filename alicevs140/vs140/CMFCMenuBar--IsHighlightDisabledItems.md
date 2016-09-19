---
title: "CMFCMenuBar::IsHighlightDisabledItems"
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
ms.assetid: ca39d4b6-12df-4804-aea1-0867e7197e30
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCMenuBar::IsHighlightDisabledItems
Indicates whether the framework highlights unavailable menu items.  
  
## Syntax  
  
```  
static BOOL IsHighlightDisabledItems();  
```  
  
## Return Value  
 `TRUE` if unavailable menu items are highlighted; otherwise `FALSE`.  
  
## Remarks  
 By default, the framework does not highlight unavailable menu items when the user positions the mouse pointer over them. Use the [CMFCMenuBar::HighlightDisabledItems](../vs140/CMFCMenuBar--HighlightDisabledItems.md) method to enable this feature.  
  
## Requirements  
 **Header:** afxmenubar.h  
  
## See Also  
 [CMFCMenuBar Class](../vs140/CMFCMenuBar-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCMenuBar::HighlightDisabledItems](../vs140/CMFCMenuBar--HighlightDisabledItems.md)