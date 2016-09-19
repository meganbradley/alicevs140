---
title: "CToolBarCtrl::SetInsertMark"
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
ms.assetid: 87617eb1-8613-42ca-928e-46241a70488c
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolBarCtrl::SetInsertMark
Sets the current insertion mark for the toolbar.  
  
## Syntax  
  
```  
  
      void SetInsertMark(  
   TBINSERTMARK* ptbim   
);  
```  
  
#### Parameters  
 `ptbim`  
 A pointer to the [TBINSERTMARK](http://msdn.microsoft.com/library/windows/desktop/bb760480) structure that contains the insertion mark.  
  
## Remarks  
 This member function implements the behavior of the Win32 message [TB_SETINSERTMARK](http://msdn.microsoft.com/library/windows/desktop/bb787437), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CToolBarCtrl Class](../vs140/CToolBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CToolBarCtrl::GetInsertMark](../vs140/CToolBarCtrl--GetInsertMark.md)