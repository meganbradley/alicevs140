---
title: "CMFCVisualManagerOffice2003::OnFillTasksGroupInterior"
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
ms.assetid: cfe4f012-3550-4be5-b484-d81fdb9a13eb
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManagerOffice2003::OnFillTasksGroupInterior
The framework calls this method when it fills the interior of a [CMFCTasksPaneTaskGroup](../vs140/CMFCTasksPaneTaskGroup-Class.md) object.  
  
## Syntax  
  
```  
virtual void OnFillTasksGroupInterior(  
   CDC* pDC,  
   CRect rect,  
   BOOL bSpecial = FALSE  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to a device context.  
  
 [in] `rect`  
 A rectangle that specifies the boundaries of the task group.  
  
 [in] `bSpecial`  
 A Boolean that indicates if the interior is filled with a special color.  
  
## Remarks  
 Override this method in a derived visual manager to customize the appearance of a task group.  
  
## Requirements  
 **Header:** afxvisualmanageroffice2003.h  
  
## See Also  
 [CMFCVisualManagerOffice2003 Class](../vs140/CMFCVisualManagerOffice2003-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)