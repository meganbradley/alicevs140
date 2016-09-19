---
title: "CMFCToolBarButton::OnBeforeDrop"
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
ms.assetid: 89a1f95e-5233-4a96-85db-86fa85ae48eb
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarButton::OnBeforeDrop
Specifies whether a user can drop the button onto the target toolbar.  
  
## Syntax  
  
```  
virtual BOOL OnBeforeDrop(  
   CMFCToolBar* pTarget  
);  
```  
  
#### Parameters  
 [in] `pTarget`  
 The target of the drag-and-drop operation.  
  
## Return Value  
 `TRUE` if the button can be dropped onto the provided target toolbar; otherwise `FALSE`.  
  
## Remarks  
 The framework calls this method before the button is dropped onto a toolbar.  
  
 The default implementation of this method returns `TRUE`. Override this method to return `FALSE` to disable the drop operation on the specified target.  
  
## Requirements  
 **Header:** afxtoolbarbutton.h  
  
## See Also  
 [CMFCToolBarButton Class](../vs140/CMFCToolBarButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)