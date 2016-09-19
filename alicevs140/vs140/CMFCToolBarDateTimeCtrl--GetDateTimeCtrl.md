---
title: "CMFCToolBarDateTimeCtrl::GetDateTimeCtrl"
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
ms.assetid: 15958fc2-5899-4f30-a5b9-7b7cebe6a672
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarDateTimeCtrl::GetDateTimeCtrl
Returns a pointer to the date and time picker control.  
  
## Syntax  
  
```  
CDateTimeCtrl* GetDateTimeCtrl() const;  
```  
  
## Return Value  
 A pointer to date and time picker control; or `NULL` if the control does not exist.  
  
## Remarks  
 The `CMFCToolBarDateTimeCtrl` class initializes the `m_pWndDateTime` data member when you insert a `CMFCToolBarDateTimeCtrl` object into a toolbar.  
  
## Requirements  
 **Header:** afxtoolbardatetimectrl.h  
  
## See Also  
 [CMFCToolBarDateTimeCtrl Class](../vs140/CMFCToolBarDateTimeCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)