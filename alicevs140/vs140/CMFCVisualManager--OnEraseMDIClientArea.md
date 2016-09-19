---
title: "CMFCVisualManager::OnEraseMDIClientArea"
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
ms.assetid: 58a69a5c-f559-4eea-a143-0d33e8ff2865
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManager::OnEraseMDIClientArea
The framework calls this method when it erases the MDI client area.  
  
## Syntax  
  
```  
virtual BOOL OnEraseMDIClientArea(  
   CDC* pDC,  
   CRect rectClient  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to a device context.  
  
 [in] `rectClient`  
 A rectangle that specifies the boundaries of the MDI client area.  
  
## Return Value  
 A reserved value. The default implementation returns `FALSE`.  
  
## Remarks  
 Override this method to execute custom code when the visual manager erases the MDI client area.  
  
## Requirements  
 **Header:** afxvisualmanager.h  
  
## See Also  
 [CMFCVisualManager Class](../vs140/CMFCVisualManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)