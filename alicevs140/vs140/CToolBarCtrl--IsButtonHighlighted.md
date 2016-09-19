---
title: "CToolBarCtrl::IsButtonHighlighted"
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
ms.assetid: 3b8864f7-32ad-4c8f-8442-8f747c9e2785
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolBarCtrl::IsButtonHighlighted
Checks the highlight state of a toolbar button.  
  
## Syntax  
  
```  
BOOL IsButtonHighlighted(  
   int nID   
) const;  
```  
  
#### Parameters  
 [in] `nID`  
 The command ID for the toolbar button.  
  
## Return Value  
 Positive integer if the button is highlighted, 0 if the button is not highlighted, or -1 if an error occurs.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CToolBarCtrl Class](../vs140/CToolBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CToolBarCtrl::IsButtonChecked](../vs140/CToolBarCtrl--IsButtonChecked.md)   
 [CToolBarCtrl::IsButtonIndeterminate](../vs140/CToolBarCtrl--IsButtonIndeterminate.md)   
 [CToolBarCtrl::IsButtonHidden](../vs140/CToolBarCtrl--IsButtonHidden.md)   
 [CToolBarCtrl::IsButtonEnabled](../vs140/CToolBarCtrl--IsButtonEnabled.md)   
 [CToolBarCtrl::IsButtonPressed](../vs140/CToolBarCtrl--IsButtonPressed.md)   
 [CToolBarCtrl::MarkButton](../vs140/CToolBarCtrl--MarkButton.md)