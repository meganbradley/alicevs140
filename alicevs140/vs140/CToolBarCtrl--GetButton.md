---
title: "CToolBarCtrl::GetButton"
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
ms.assetid: e2808bd8-fb89-4069-83a9-79ce374dfcb4
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolBarCtrl::GetButton
Retrieves information about the specified button in a toolbar control.  
  
## Syntax  
  
```  
  
      BOOL GetButton(  
   int nIndex,  
   LPTBBUTTON lpButton   
) const;  
```  
  
#### Parameters  
 `nIndex`  
 Zero-based index of the button for which to retrieve information.  
  
 `lpButton`  
 Address of the `TBBUTTON` structure that is to receive a copy of the button information. See [CToolBarCtrl::AddButtons](../vs140/CToolBarCtrl--AddButtons.md) for information about the `TBBUTTON` structure.  
  
## Return Value  
 Nonzero if successful; otherwise zero.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CToolBarCtrl Class](../vs140/CToolBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CToolBarCtrl::GetState](../vs140/CToolBarCtrl--GetState.md)   
 [CToolBarCtrl::SetState](../vs140/CToolBarCtrl--SetState.md)   
 [CToolBarCtrl::GetButtonCount](../vs140/CToolBarCtrl--GetButtonCount.md)   
 [CToolBarCtrl::GetItemRect](../vs140/CToolBarCtrl--GetItemRect.md)   
 [CToolBarCtrl::CommandToIndex](../vs140/CToolBarCtrl--CommandToIndex.md)   
 [CToolBarCtrl::AddButtons](../vs140/CToolBarCtrl--AddButtons.md)   
 [CToolBarCtrl::InsertButton](../vs140/CToolBarCtrl--InsertButton.md)