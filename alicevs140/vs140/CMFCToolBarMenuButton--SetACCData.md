---
title: "CMFCToolBarMenuButton::SetACCData"
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
ms.assetid: 4552da86-a8e1-4a49-89cd-634b5a5f2533
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarMenuButton::SetACCData
Sets the accessibility data for the ribbon element.  
  
## Syntax  
  
```  
virtual BOOL SetACCData(  
   CWnd* pParent,  
   CAccessibilityData& data  
);   
```  
  
#### Parameters  
 `pParent`  
 The parent window for the ribbon element.  
  
 `data`  
 The accessibility data for the ribbon element.  
  
## Return Value  
 Always returns `TRUE`.  
  
## Remarks  
 By default this method sets the accessibility data for the ribbon element and always returns `TRUE`. Override this method to set the accessibility data and return a value that indicates success or failure.  
  
## Requirements  
 **Header:** afxtoolbarmenubutton.h  
  
## See Also  
 [CMFCToolBarMenuButton Class](../vs140/CMFCToolBarMenuButton-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)