---
title: "CToolBarCtrl::GetInsertMark"
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
ms.assetid: 14fa5ff2-1459-47a2-9544-657051350fe3
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolBarCtrl::GetInsertMark
Retrieves the current insertion mark for the toolbar.  
  
## Syntax  
  
```  
  
      void GetInsertMark(  
   TBINSERTMARK* ptbim   
) const;  
```  
  
#### Parameters  
 `ptbim`  
 A pointer to a [TBINSERTMARK](http://msdn.microsoft.com/library/windows/desktop/bb760480) structure that receives the insertion mark.  
  
## Remarks  
 This member function implements the behavior of the Win32 message [TB_GETINSERTMARK](http://msdn.microsoft.com/library/windows/desktop/bb787338), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CToolBarCtrl Class](../vs140/CToolBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CToolBarCtrl::SetInsertMark](../vs140/CToolBarCtrl--SetInsertMark.md)