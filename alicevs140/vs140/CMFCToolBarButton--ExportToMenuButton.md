---
title: "CMFCToolBarButton::ExportToMenuButton"
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
ms.assetid: 40f7b2bf-d7bb-48ce-a984-89d5f241c93d
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarButton::ExportToMenuButton
Copies text from the toolbar button to a menu.  
  
## Syntax  
  
```  
virtual BOOL ExportToMenuButton(  
   CMFCToolBarMenuButton& menuButton   
) const;  
```  
  
#### Parameters  
 [in] `menuButton`  
 A reference to the target menu button.  
  
## Return Value  
 This method returns `TRUE`.  
  
## Remarks  
 The framework calls this method to copy the text from a toolbar button to a menu button. The default implementation copies the text label of the button. If the text label is empty, this method copies the tooltip text of the button.  
  
 The default implementation of this method returns `TRUE`. Override this method if you want to take additional actions when the framework converts an object that is derived from [CMFCToolBarButton Class](../vs140/CMFCToolBarButton-Class.md) to a menu button.  
  
## Requirements  
 **Header:** afxtoolbarbutton.h  
  
## See Also  
 [CMFCToolBarButton Class](../vs140/CMFCToolBarButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBarMenuButton Class](../vs140/CMFCToolBarMenuButton-Class.md)