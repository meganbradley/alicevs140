---
title: "CListCtrl::SetItemCountEx"
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
ms.assetid: c50a684d-c9a4-467c-940c-2da57a94a8aa
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::SetItemCountEx
Sets the item count for a virtual list view control.  
  
## Syntax  
  
```  
  
      BOOL SetItemCountEx(  
   int iCount,  
   DWORD dwFlags = LVSICF_NOINVALIDATEALL   
);  
```  
  
#### Parameters  
 `iCount`  
 Number of items that the control will ultimately contain.  
  
 `dwFlags`  
 Specifies the behavior of the list view control after resetting the item count. This value can be a combination of the following:  
  
-   **LVSICF_NOINVALIDATEALL** The list view control will not repaint unless affected items are currently in view. This is the default value.  
  
-   **LVSICF_NOSCROLL** The list view control will not change the scroll position when the item count changes.  
  
## Return Value  
 Nonzero if successful; otherwise zero.  
  
## Remarks  
 This member function implements the behavior of the Win32 macro, [ListView_SetItemCountEx](http://msdn.microsoft.com/library/windows/desktop/bb775095), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]and should only be called for virtual list views.  
  
## Example  
 [!CODE [NVC_MFC_CListCtrl#36](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListCtrl#36)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListCtrl::SetItemCount](../vs140/CListCtrl--SetItemCount.md)