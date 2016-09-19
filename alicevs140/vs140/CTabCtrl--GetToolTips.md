---
title: "CTabCtrl::GetToolTips"
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
ms.assetid: ea2fc9b2-1195-4e61-8c44-8cffa0b3c0e4
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTabCtrl::GetToolTips
Retrieves the handle of the tool tip control associated with a tab control.  
  
## Syntax  
  
```  
  
CToolTipCtrl* GetToolTips( ) const;  
```  
  
## Return Value  
 Handle of the tool tip control if successful; otherwise **NULL**.  
  
## Remarks  
 A tab control creates a tool tip control if it has the **TCS_TOOLTIPS** style. You can also assign a tool tip control to a tab control by using the `SetToolTips` member function.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CTabCtrl Class](../vs140/CTabCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTabCtrl::SetToolTips](../vs140/CTabCtrl--SetToolTips.md)   
 [CTabCtrl::Create](../vs140/CTabCtrl--Create.md)