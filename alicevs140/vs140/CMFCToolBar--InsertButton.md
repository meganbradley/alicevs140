---
title: "CMFCToolBar::InsertButton"
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
ms.assetid: c4736be1-a623-4045-8353-278255bfd1d0
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::InsertButton
Inserts a button into the toolbar.  
  
## Syntax  
  
```  
virtual int InsertButton(  
   const CMFCToolBarButton& button,  
   INT_PTR iInsertAt=-1   
);  
virtual int InsertButton(  
   CMFCToolBarButton* pButton,  
   int iInsertAt=-1   
);  
```  
  
#### Parameters  
 [in] `button`  
 Specifies the button to insert.  
  
 [in] `iInsertAt`  
 Specifies the zero-based position to insert the button at.  
  
## Return Value  
 The position at which the button was inserted or -1 if an error occurs.  
  
## Remarks  
 If `iInsertAt` is -1, this method adds the button to the end of the list of toolbar buttons.  
  
 Call the [CMFCToolBar::InsertSeparator](../vs140/CMFCToolBar--InsertSeparator.md) method to insert a separator into the toolbar.  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBar::InsertSeparator](../vs140/CMFCToolBar--InsertSeparator.md)