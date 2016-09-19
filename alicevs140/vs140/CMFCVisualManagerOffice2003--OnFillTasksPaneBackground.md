---
title: "CMFCVisualManagerOffice2003::OnFillTasksPaneBackground"
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
ms.assetid: ebdf686a-3678-4068-83e7-8a99be7f8113
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManagerOffice2003::OnFillTasksPaneBackground
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
 Override this method in a derived visual manager to customize the appearance of a [CMFCTasksPane](../vs140/CMFCTasksPane-Class.md) object.  
  
## Requirements  
 **Header:** afxvisualmanageroffice2003.h  
  
## See Also  
 [CMFCVisualManagerOffice2003 Class](../vs140/CMFCVisualManagerOffice2003-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)