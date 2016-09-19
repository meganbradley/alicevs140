---
title: "CListCtrl::SetHotCursor"
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
ms.assetid: 166bdf64-790a-4614-9e7c-1a46cc93f6fe
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::SetHotCursor
Sets the cursor used when hot tracking is enabled for a list view control.  
  
## Syntax  
  
```  
  
      HCURSOR SetHotCursor(  
   HCURSOR hc   
);  
```  
  
#### Parameters  
 *hc*  
 A handle to a cursor resource, used to represent the hot cursor.  
  
## Return Value  
 The handle to the previous hot cursor resource being used by the list view control.  
  
## Remarks  
 This member function implements the behavior of the Win32 macro, [ListView_SetHotCursor](http://msdn.microsoft.com/library/windows/desktop/bb775082), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 The hot cursor, only visible when hover selection is enabled, appears as the cursor passes over any list view item. Hover selection is enabled by setting the **LVS_EX_TRACKSELECT** extended style.  
  
## Example  
 See the example for [CListCtrl::GetHotCursor](../vs140/CListCtrl--GetHotCursor.md).  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListCtrl::GetHotCursor](../vs140/CListCtrl--GetHotCursor.md)   
 [CListCtrl::GetHotItem](../vs140/CListCtrl--GetHotItem.md)