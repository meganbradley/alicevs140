---
title: "CListCtrl::SetHotItem"
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
ms.assetid: c2f0354d-e522-40b8-af55-712295945108
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::SetHotItem
Sets the current hot item of a list view control.  
  
## Syntax  
  
```  
  
      int SetHotItem(  
   int iIndex   
);  
```  
  
#### Parameters  
 `iIndex`  
 Zero-based index of the item to be set as the hot item.  
  
## Return Value  
 The zero-based index of the previously hot item.  
  
## Remarks  
 This member function implements the behavior of the Win32 macro, [ListView_SetHotItem](http://msdn.microsoft.com/library/windows/desktop/bb775083), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 See the example for [CListCtrl::GetHotItem](../vs140/CListCtrl--GetHotItem.md).  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListCtrl::GetHotCursor](../vs140/CListCtrl--GetHotCursor.md)   
 [CListCtrl::GetHotItem](../vs140/CListCtrl--GetHotItem.md)