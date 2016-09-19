---
title: "CToolBarCtrl::GetInsertMarkColor"
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
ms.assetid: 613726b0-ac12-4bdc-bb56-d2deadbfb5cf
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolBarCtrl::GetInsertMarkColor
Retrieves the color used to draw the insertion mark for the toolbar.  
  
## Syntax  
  
```  
  
COLORREF GetInsertMarkColor( ) const;  
  
```  
  
## Return Value  
 A **COLORREF** value that contains the current insertion mark color.  
  
## Remarks  
 This member function implements the behavior of the Win32 message [TB_GETINSERTMARKCOLOR](http://msdn.microsoft.com/library/windows/desktop/bb787339), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CToolBarCtrl Class](../vs140/CToolBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CToolBarCtrl::SetInsertMarkColor](../vs140/CToolBarCtrl--SetInsertMarkColor.md)