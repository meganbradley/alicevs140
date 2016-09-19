---
title: "CMFCVisualManagerOffice2003::OnUpdateSystemColors"
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
ms.assetid: 9886fa01-cc4c-4269-a1da-52997027f9fc
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManagerOffice2003::OnUpdateSystemColors
The framework calls this function when the system colors change.  
  
## Syntax  
  
```  
virtual void OnUpdateSystemColors();  
```  
  
## Remarks  
 The framework calls this method as a part of processing the `WM_SYSCOLORCHANGE` message. Override this method in a derived visual manager if you want to execute custom code when the colors change in your application.  
  
## Requirements  
 **Header:** afxvisualmanageroffice2003.h  
  
## See Also  
 [CMFCVisualManagerOffice2003 Class](../vs140/CMFCVisualManagerOffice2003-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)