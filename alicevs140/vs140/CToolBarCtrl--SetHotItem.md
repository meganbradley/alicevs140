---
title: "CToolBarCtrl::SetHotItem"
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
ms.assetid: 53cbad57-3c98-4e2d-8e45-d12727612d66
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolBarCtrl::SetHotItem
Sets the hot item in a toolbar.  
  
## Syntax  
  
```  
  
      int SetHotItem(  
   int nHot   
);  
```  
  
#### Parameters  
 *nHot*  
 The zero-based index number of the item that will be made hot. If this value is -1, none of the items will be hot.  
  
## Return Value  
 The index of the previous hot item, or -1 if there was no hot item.  
  
## Remarks  
 This member function implements the behavior of the Win32 message [TB_SETHOTITEM](http://msdn.microsoft.com/library/windows/desktop/bb787431), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CToolBarCtrl Class](../vs140/CToolBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CToolBarCtrl::GetHotItem](../vs140/CToolBarCtrl--GetHotItem.md)