---
title: "CReBarCtrl::GetDropTarget"
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
ms.assetid: bfea8bae-554c-444b-858c-b84b4c939fc3
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CReBarCtrl::GetDropTarget
Implements the behavior of the Win32 message [RB_GETDROPTARGET](http://msdn.microsoft.com/library/windows/desktop/bb774463), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Syntax  
  
```  
  
IDropTarget* GetDropTarget( ) const;  
  
```  
  
## Return Value  
 A pointer to an [IDropTarget](http://msdn.microsoft.com/library/windows/desktop/ms679679) interface.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CReBarCtrl Class](../vs140/CReBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)