---
title: "CMFCVisualManager::OnDrawTasksGroupCaption"
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
ms.assetid: 616dac74-5072-477a-944f-9b353041684e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManager::OnDrawTasksGroupCaption
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
 A pointer to a `CMFCTasksPaneTaskGroup` object. The framework draws the caption for this group.  
  
 [in] `bIsHighlighted`  
 A Boolean parameter that indicates whether the group is highlighted.  
  
 [in] `bIsSelected`  
 A Boolean parameter that indicates whether the group is currently selected.  
  
 [in] `bCanCollapse`  
 A Boolean parameter that indicates whether the group can be collapsed.  
  
## Remarks  
 The task groups appear on the [CMFCTasksPane](../vs140/CMFCTasksPane-Class.md) object.  
  
 Override this method in a derived class to customize the caption for a `CMFCTasksPaneTaskGroup`.  
  
## Requirements  
 **Header:** afxvisualmanager.h  
  
## See Also  
 [CMFCVisualManager Class](../vs140/CMFCVisualManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCTasksPaneTaskGroup Class](../vs140/CMFCTasksPaneTaskGroup-Class.md)