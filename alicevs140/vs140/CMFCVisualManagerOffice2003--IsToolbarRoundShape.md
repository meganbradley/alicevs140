---
title: "CMFCVisualManagerOffice2003::IsToolbarRoundShape"
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
ms.assetid: 80037f8b-d279-4a9c-9c5f-c804383a66fa
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManagerOffice2003::IsToolbarRoundShape
Indicates whether a specified toolbar is round.  
  
## Syntax  
  
```  
virtual BOOL IsToolbarRoundShape(  
   CMFCToolBar* pToolBar  
);  
```  
  
#### Parameters  
 [in] `pToolBar`  
 Pointer to the toolbar in question.  
  
## Return Value  
 Returns `TRUE` if the toolbar is round, or `FALSE` if it is a menu bar.  
  
## Remarks  
  
## Requirements  
 **Header:** afxvisualmanageroffice2003.h  
  
## See Also  
 [CMFCVisualManagerOffice2003 Class](../vs140/CMFCVisualManagerOffice2003-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)