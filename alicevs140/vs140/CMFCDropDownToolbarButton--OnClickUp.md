---
title: "CMFCDropDownToolbarButton::OnClickUp"
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
ms.assetid: d0c2fa3a-1b89-4982-9c30-ca7c9506c608
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCDropDownToolbarButton::OnClickUp
Called by the framework when the user releases the mouse button.  
  
## Syntax  
  
```  
virtual BOOL OnClickUp();  
```  
  
## Return Value  
 Nonzero if the button processes the click message; otherwise 0.  
  
## Remarks  
 This method extends the base class implementation, [CMFCToolBarButton::OnClickUp](../vs140/CMFCToolBarButton--OnClickUp.md), by updating the state of the drop-down toolbar.  
  
 This method stops the drop-down toolbar timer if it is active. It closes the drop-down toolbar if it is open.  
  
 For more information about the drop-down toolbar and drop-down toolbar timer, see [CMFCDropDownToolbarButton::OnClick](../vs140/CMFCDropDownToolbarButton--OnClick.md).  
  
## Requirements  
 **Header:** afxdropdowntoolbar.h  
  
## See Also  
 [CMFCDropDownToolbarButton Class](../vs140/CMFCDropDownToolbarButton-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBarButton::OnClickUp](../vs140/CMFCToolBarButton--OnClickUp.md)   
 [CMFCDropDownToolbarButton::OnClick](../vs140/CMFCDropDownToolbarButton--OnClick.md)