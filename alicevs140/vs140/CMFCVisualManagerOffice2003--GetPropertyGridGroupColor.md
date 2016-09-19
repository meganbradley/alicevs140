---
title: "CMFCVisualManagerOffice2003::GetPropertyGridGroupColor"
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
ms.assetid: 62789e43-345c-4b9f-85a2-f58540bdd9ee
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManagerOffice2003::GetPropertyGridGroupColor
The framework calls this method to get the background color of a property list.  
  
## Syntax  
  
```  
virtual COLORREF GetPropertyGridGroupColor(  
   CMFCPropertyGridCtrl* pPropList  
);  
```  
  
#### Parameters  
 [in] `pPropList`  
 A pointer to the property list that the framework is drawing.  
  
## Return Value  
 Returns the background color of `pPropList`.  
  
## Remarks  
 Override this function to customize the background color of a property list in your application.  
  
## Requirements  
 **Header:** afxvisualmanageroffice2003.h  
  
## See Also  
 [CMFCVisualManagerOffice2003 Class](../vs140/CMFCVisualManagerOffice2003-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)