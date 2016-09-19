---
title: "CMFCToolBar::ButtonToIndex"
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
ms.assetid: 15471f19-7a31-4144-9c6c-c8b54cf18bc2
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::ButtonToIndex
Returns the index of a specified [CMFCToolBarButton](../vs140/CMFCToolBarButton-Class.md) object in this toolbar.  
  
## Syntax  
  
```  
int ButtonToIndex(  
   const CMFCToolBarButton* pButton   
) const;  
```  
  
#### Parameters  
 [in] `pButton`  
 A pointer to the toolbar button object.  
  
## Return Value  
 Index of `pButton` in the internal list of toolbar buttons; or -1 if the specified button is not on this toolbar.  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)