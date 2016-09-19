---
title: "CMFCVisualManager::OnFillTasksPaneBackground"
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
ms.assetid: dc0285d8-d3e3-41aa-91f6-e1c4e0fbd393
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManager::OnFillTasksPaneBackground
The framework calls this method when it fills the background of a [CMFCTasksPane](../vs140/CMFCTasksPane-Class.md) control.  
  
## Syntax  
  
```  
virtual void OnFillTasksPaneBackground(  
   CDC* pDC,  
   CRect rectWorkArea  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to a device context.  
  
 [in] `rectWorkArea`  
 A rectangle that specifies the boundaries of the task pane.  
  
## Remarks  
 Override this method in a derived visual manager to customize the appearance of a `CMFCTasksPane` object.  
  
## Requirements  
 **Header:** afxvisualmanager.h  
  
## See Also  
 [CMFCVisualManager Class](../vs140/CMFCVisualManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCTasksPane Class](../vs140/CMFCTasksPane-Class.md)