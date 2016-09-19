---
title: "CToolBarCtrl::GetRows"
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
ms.assetid: 17d22154-ec68-4199-ba37-41fe03b0cb63
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolBarCtrl::GetRows
Retrieves the number of rows of buttons currently displayed by the toolbar control.  
  
## Syntax  
  
```  
  
int GetRows( ) const;  
```  
  
## Return Value  
 Number of rows of buttons currently displayed on the toolbar.  
  
## Remarks  
 Note that the number of rows will always be one unless the toolbar was created with the `TBSTYLE_WRAPABLE` style.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CToolBarCtrl Class](../vs140/CToolBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CToolBarCtrl::Create](../vs140/CToolBarCtrl--Create.md)   
 [CToolBarCtrl::SetRows](../vs140/CToolBarCtrl--SetRows.md)