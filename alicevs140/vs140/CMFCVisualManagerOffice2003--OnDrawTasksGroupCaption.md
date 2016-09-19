---
title: "CMFCVisualManagerOffice2003::OnDrawTasksGroupCaption"
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
ms.assetid: ae42a2a8-27a7-4937-8ef4-c34b1f21b122
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManagerOffice2003::OnDrawTasksGroupCaption
The framework calls this method when it draws the caption for a [CMFCTasksPaneTaskGroup](../vs140/CMFCTasksPaneTaskGroup-Class.md) object.  
  
## Syntax  
  
```  
virtual void OnDrawTasksGroupCaption(  
   CDC* pDC,  
   CMFCTasksPaneTaskGroup* pGroup,  
   BOOL bIsHighlighted = FALSE,  
   BOOL bIsSelected = FALSE,  
   BOOL bCanCollapse = FALSE  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to a device context.  
  
 [in] `pGroup`  
 A pointer to a [CMFCTasksPaneTaskGroup](../vs140/CMFCTasksPaneTaskGroup-Class.md) object. The framework draws the caption for this group.  
  
 [in] `bIsHighlighted`  
 A Boolean parameter that indicates whether the group is highlighted.  
  
 [in] `bIsSelected`  
 A Boolean parameter that indicates whether the group is currently selected.  
  
 [in] `bCanCollapse`  
 A Boolean parameter that indicates whether the group can be collapsed.  
  
## Remarks  
 Override this method in a derived class to customize the caption for a `CMFCTasksPaneTaskGroup`.  
  
## Requirements  
 **Header:** afxvisualmanageroffice2003.h  
  
## See Also  
 [CMFCVisualManagerOffice2003 Class](../vs140/CMFCVisualManagerOffice2003-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)