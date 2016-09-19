---
title: "CMFCToolBar::GetButtonSize"
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
ms.assetid: f710a4b6-4aa7-4370-8e48-b7cd8ae1885b
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::GetButtonSize
Returns the dimensions of each button on the toolbar.  
  
## Syntax  
  
```  
CSize GetButtonSize() const;  
```  
  
## Return Value  
 A [CSize](../vs140/CSize-Class.md) object that specifies the dimensions of each button on the toolbar.  
  
## Remarks  
 Call [CMFCToolBar::SetSizes](../vs140/CMFCToolBar--SetSizes.md) or [CMFCToolBar::SetLockedSizes](../vs140/CMFCToolBar--SetLockedSizes.md) to set the dimensions of each button on the toolbar.  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)