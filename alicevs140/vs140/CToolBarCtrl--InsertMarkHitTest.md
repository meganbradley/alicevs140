---
title: "CToolBarCtrl::InsertMarkHitTest"
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
ms.assetid: 0bca462e-3027-4ddc-9fb0-59ab593e7708
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolBarCtrl::InsertMarkHitTest
Retrieves the insertion mark information for a point in a toolbar.  
  
## Syntax  
  
```  
  
      BOOL InsertMarkHitTest(  
   LPPOINT ppt,  
   LPTBINSERTMARK ptbim   
) const;  
```  
  
#### Parameters  
 `ppt`  
 A pointer to a [POINT](http://msdn.microsoft.com/library/windows/desktop/dd162805) structure that contains the hit test coordinates, relative to the client area of the toolbar.  
  
 `ptbim`  
 A pointer to a [TBINSERTMARK](http://msdn.microsoft.com/library/windows/desktop/bb760480) structure that receives the insertion mark information.  
  
## Return Value  
 Nonzero if successful; otherwise zero.  
  
## Remarks  
 This member function implements the behavior of the Win32 message [TB_INSERTMARKHITTEST](http://msdn.microsoft.com/library/windows/desktop/bb787367), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CToolBarCtrl Class](../vs140/CToolBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CToolBarCtrl::GetInsertMark](../vs140/CToolBarCtrl--GetInsertMark.md)   
 [CToolBarCtrl::SetInsertMark](../vs140/CToolBarCtrl--SetInsertMark.md)