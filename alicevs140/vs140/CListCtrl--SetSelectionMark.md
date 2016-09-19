---
title: "CListCtrl::SetSelectionMark"
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
ms.assetid: cc5ddcd6-974c-4e0c-a463-3a04d230f48a
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::SetSelectionMark
Sets the selection mark of a list view control.  
  
## Syntax  
  
```  
  
      int SetSelectionMark(  
   int iIndex   
);  
```  
  
#### Parameters  
 `iIndex`  
 The zero-based index of the first item in a multiple selection.  
  
## Return Value  
 The previous selection mark, or -1 if there was no selection mark.  
  
## Remarks  
 This member function implements the behavior of the Win32 macro, [ListView_SetSelectionMark](http://msdn.microsoft.com/library/windows/desktop/bb775112), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 See the example for [CListCtrl::GetSelectionMark](../vs140/CListCtrl--GetSelectionMark.md).  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListCtrl::GetSelectionMark](../vs140/CListCtrl--GetSelectionMark.md)