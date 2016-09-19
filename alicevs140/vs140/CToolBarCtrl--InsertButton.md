---
title: "CToolBarCtrl::InsertButton"
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
ms.assetid: c5b11606-5711-4e14-a7ff-276a45f86f57
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolBarCtrl::InsertButton
Inserts a button in a toolbar control.  
  
## Syntax  
  
```  
  
      BOOL InsertButton(  
   int nIndex,  
   LPTBBUTTON lpButton   
);  
```  
  
#### Parameters  
 `nIndex`  
 Zero-based index of a button. This function inserts the new button to the left of this button.  
  
 `lpButton`  
 Address of a `TBBUTTON` structure containing information about the button to insert. See [CToolBarCtrl::AddButtons](../vs140/CToolBarCtrl--AddButtons.md) for a description of the `TBBUTTON` structure.  
  
## Return Value  
 Nonzero if successful; otherwise zero.  
  
## Remarks  
 The image and/or string whose index you provide must have previously been added to the toolbar control's list using [AddBitmap](../vs140/CToolBarCtrl--AddBitmap.md), [AddString](../vs140/CToolBarCtrl--AddString.md), and/or [AddStrings](../vs140/CToolBarCtrl--AddStrings.md).  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CToolBarCtrl Class](../vs140/CToolBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CToolBarCtrl::AddButtons](../vs140/CToolBarCtrl--AddButtons.md)   
 [CToolBarCtrl::DeleteButton](../vs140/CToolBarCtrl--DeleteButton.md)   
 [CToolBarCtrl::AddBitmap](../vs140/CToolBarCtrl--AddBitmap.md)   
 [CToolBarCtrl::AddString](../vs140/CToolBarCtrl--AddString.md)   
 [CToolBarCtrl::AddStrings](../vs140/CToolBarCtrl--AddStrings.md)