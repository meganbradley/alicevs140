---
title: "CMFCToolBar::IsLocked"
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
ms.assetid: e16a9849-7355-41df-a970-dfa5d2425365
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::IsLocked
Determines whether the toolbar is locked.  
  
## Syntax  
  
```  
BOOL IsLocked() const;  
```  
  
## Return Value  
 `TRUE` if the toolbar is locked; otherwise, `FALSE`.  
  
## Remarks  
 This method returns `TRUE` when the user cannot perform customization tasks such as repositioning toolbar buttons.  
  
 Locked toolbars use separate image lists. For more information about these image lists, see [CMFCToolBar::LoadBitmapEx](../vs140/CMFCToolBar--LoadBitmapEx.md).  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBar::LoadBitmapEx](../vs140/CMFCToolBar--LoadBitmapEx.md)