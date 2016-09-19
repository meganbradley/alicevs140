---
title: "CToolBarCtrl::SetInsertMarkColor"
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
ms.assetid: f17454a2-78dd-48e1-81a3-ce4c4f5e9501
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolBarCtrl::SetInsertMarkColor
Sets the color used to draw the insertion mark for the toolbar.  
  
## Syntax  
  
```  
  
      COLORREF SetInsertMarkColor(  
   COLORREF clrNew   
);  
```  
  
#### Parameters  
 `clrNew`  
 A **COLORREF** value that contains the new insertion mark color.  
  
## Return Value  
 A **COLORREF** value that contains the previous insertion mark color.  
  
## Remarks  
 This member function implements the behavior of the Win32 message [TB_SETINSERTMARKCOLOR](http://msdn.microsoft.com/library/windows/desktop/bb787439), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CToolBarCtrl Class](../vs140/CToolBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CToolBarCtrl::GetInsertMarkColor](../vs140/CToolBarCtrl--GetInsertMarkColor.md)