---
title: "CToolBarCtrl::GetHotItem"
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
ms.assetid: 9bf1a576-f197-4f00-aa35-fda6af51c9da
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolBarCtrl::GetHotItem
Retrieves the index of the hot item in a toolbar.  
  
## Syntax  
  
```  
  
int GetHotItem( ) const;  
  
```  
  
## Return Value  
 The zero-based index of the hot item in a toolbar.  
  
## Remarks  
 This member function implements the behavior of the Win32 message [TB_GETHOTITEM](http://msdn.microsoft.com/library/windows/desktop/bb787336), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CToolBarCtrl Class](../vs140/CToolBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CToolBarCtrl::SetHotItem](../vs140/CToolBarCtrl--SetHotItem.md)