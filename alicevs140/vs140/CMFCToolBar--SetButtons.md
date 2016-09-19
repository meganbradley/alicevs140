---
title: "CMFCToolBar::SetButtons"
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
ms.assetid: 08e97608-1652-4777-bd63-6dba16ec1597
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::SetButtons
Sets the buttons for the toolbar.  
  
## Syntax  
  
```  
virtual BOOL SetButtons(  
   const UINT* lpIDArray,  
   int nIDCount,  
   BOOL bRemapImages=TRUE   
);  
```  
  
#### Parameters  
 [in] `lpIDArray`  
 A pointer to the array of command IDs of the buttons to insert.  
  
 [in] `nIDCount`  
 The number of items in `lpIDArray`.  
  
 [in] `bRemapImages`  
 A Boolean value that specifies whether to associate the existing button images with the inserted buttons. If this parameter is `TRUE`, the images are remapped.  
  
## Return Value  
 Nonzero if the method succeeds; otherwise 0.  
  
## Remarks  
 Call this method to remove existing buttons from a toolbar and insert a collection of new buttons.  
  
 This method adds the **Customize** button to the toolbar and sends the `AFX_WM_RESETTOOLBAR` message to the parent window of the toolbar. For more information about the **Customize** button, see [CMFCToolBar::EnableCustomizeButton](../vs140/CMFCToolBar--EnableCustomizeButton.md).  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBar::EnableCustomizeButton](../vs140/CMFCToolBar--EnableCustomizeButton.md)