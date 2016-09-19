---
title: "CToolBarCtrl::GetItemRect"
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
ms.assetid: b12755b6-ecb5-440f-ba9d-52e824199235
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolBarCtrl::GetItemRect
Retrieves the bounding rectangle of a button in a toolbar control.  
  
## Syntax  
  
```  
  
      BOOL GetItemRect(  
   int nIndex,  
   LPRECT lpRect   
) const;  
```  
  
#### Parameters  
 `nIndex`  
 Zero-based index of the button for which to retrieve information.  
  
 `lpRect`  
 Address of a [RECT](http://msdn.microsoft.com/library/windows/desktop/dd162897) structure or a [CRect](../vs140/CRect-Class.md) object that receives the coordinates of the bounding rectangle.  
  
## Return Value  
 Nonzero if successful; otherwise zero.  
  
## Remarks  
 This function does not retrieve the bounding rectangle for buttons whose state is set to `TBSTATE_HIDDEN`.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CToolBarCtrl Class](../vs140/CToolBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CToolBarCtrl::GetButton](../vs140/CToolBarCtrl--GetButton.md)   
 [CToolBarCtrl::GetButtonCount](../vs140/CToolBarCtrl--GetButtonCount.md)   
 [CToolBarCtrl::GetState](../vs140/CToolBarCtrl--GetState.md)   
 [CToolBarCtrl::SetButtonSize](../vs140/CToolBarCtrl--SetButtonSize.md)   
 [CToolBarCtrl::SetBitmapSize](../vs140/CToolBarCtrl--SetBitmapSize.md)