---
title: "CMFCToolBarButton::CanBeDropped"
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
ms.assetid: 44181450-66f4-4a6a-8454-921bffe4f384
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarButton::CanBeDropped
Specifies whether a user can position a button on a toolbar or menu during customization.  
  
## Syntax  
  
```  
virtual BOOL CanBeDropped(  
   CMFCToolBar* pToolbar  
);  
```  
  
#### Parameters  
 [in] `pToolbar`  
 Unused.  
  
## Return Value  
 This method returns `TRUE`.  
  
## Remarks  
 By default, a toolbar button can be dropped on every customizable (that is, non-locked) toolbar.  
  
 The default implementation of this method returns `TRUE`. Override this method and return `FALSE` if you want to prevent the user from repositioning the button.  
  
## Requirements  
 **Header:** afxtoolbarbutton.h  
  
## See Also  
 [CMFCToolBarButton Class](../vs140/CMFCToolBarButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)