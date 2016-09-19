---
title: "CMFCVisualManager::OnDrawTasksGroupAreaBorder"
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
ms.assetid: 41a78615-a85b-4134-bfcf-83e60b370dfd
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManager::OnDrawTasksGroupAreaBorder
The framework calls this method when it draws a border around a group on a [CMFCTasksPane Class](../vs140/CMFCTasksPane-Class.md).  
  
## Syntax  
  
```  
virtual void OnDrawTasksGroupAreaBorder(  
   CDC* pDC,  
   CRect rect,  
   BOOL bSpecial = FALSE,  
   BOOL bNoTitle = FALSE  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to a device context.  
  
 [in] `rect`  
 A rectangle that specifies the boundaries of the group area on the task pane.  
  
 [in] `bSpecial`  
 A Boolean parameter that specifies if the border is highlighted. A value of `TRUE` indicates that the border is highlighted.  
  
 [in] `bNoTitle`  
 A Boolean parameter that specifies whether the group area has a title. A value of `TRUE` indicates that the group area does not have a title.  
  
## Remarks  
 Override this function in a derived class to customize the border around a group area on the task pane.  
  
## Requirements  
 **Header:** afxvisualmanager.h  
  
## See Also  
 [CMFCVisualManager Class](../vs140/CMFCVisualManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCTasksPane Class](../vs140/CMFCTasksPane-Class.md)