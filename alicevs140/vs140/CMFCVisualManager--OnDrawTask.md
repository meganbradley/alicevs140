---
title: "CMFCVisualManager::OnDrawTask"
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
ms.assetid: 5f71a094-a322-45f6-b9b8-8166b19fe2fa
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManager::OnDrawTask
The framework calls this method when it draws a [CMFCTasksPane](../vs140/CMFCTasksPane-Class.md) object.  
  
## Syntax  
  
```  
virtual void OnDrawTask(  
   CDC* pDC,  
   CMFCTasksPaneTask* pTask,  
   CImageList* pIcons,  
   BOOL bIsHighlighted = FALSE,  
   BOOL bIsSelected = FALSE  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to a device context.  
  
 [in] `pTask`  
 A pointer to a [CMFCTasksPaneTask](../vs140/CMFCTasksPaneTask-Class.md) object. The framework draws this task.  
  
 [in] `pIcons`  
 A pointer to the image list associated with the task pane. Each task contains an index for an image in this list.  
  
 [in] `bIsHighlighted`  
 A Boolean parameter that specifies whether the displayed task is highlighted.  
  
 [in] `bIsSelected`  
 A Boolean parameter that specifies whether the displayed task is selected.  
  
## Remarks  
 The framework displays tasks on the task bar as both an icon and text. The `pIcons` parameter contains the icon for the task indicated by `pTask`.  
  
 Override this method in a derived class to customize the appearance of tasks on the task bar.  
  
## Requirements  
 **Header:** afxvisualmanager.h  
  
## See Also  
 [CMFCVisualManager Class](../vs140/CMFCVisualManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCTasksPane Class](../vs140/CMFCTasksPane-Class.md)   
 [CMFCTasksPaneTask Class](../vs140/CMFCTasksPaneTask-Class.md)