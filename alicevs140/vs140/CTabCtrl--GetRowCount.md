---
title: "CTabCtrl::GetRowCount"
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
ms.assetid: 38fe8a38-d729-4aec-90c5-e16f761e6fa0
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTabCtrl::GetRowCount
Retrieves the current number of rows in a tab control.  
  
## Syntax  
  
```  
  
int GetRowCount( ) const;  
```  
  
## Return Value  
 The number of rows of tabs in the tab control.  
  
## Remarks  
 Only tab controls that have the **TCS_MULTILINE** style can have multiple rows of tabs.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CTabCtrl Class](../vs140/CTabCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTabCtrl::Create](../vs140/CTabCtrl--Create.md)