---
title: "CListCtrl::GetColumnOrderArray"
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
ms.assetid: b05c507c-6b9a-4b10-ab18-c7547edfe51e
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::GetColumnOrderArray
Retrieves the column order (left to right) of a list view control.  
  
## Syntax  
  
```  
  
      BOOL GetColumnOrderArray(  
   LPINT piArray,  
   int iCount = -1   
);  
```  
  
#### Parameters  
 `piArray`  
 A pointer to a buffer that will contain the index values of the columns in the list view control. The buffer must be large enough to contain the total number of columns in the list view control.  
  
 `iCount`  
 Number of columns in the list view control. If this parameter is -1, the number of columns is automatically retrieved by the framework.  
  
## Return Value  
 Nonzero if successful; otherwise zero.  
  
## Remarks  
 This member function implements the behavior of the Win32 macro, [ListView_GetColumnOrderArray](http://msdn.microsoft.com/library/windows/desktop/bb761254), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CListCtrl#12](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListCtrl#12)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListCtrl::SetColumnOrderArray](../vs140/CListCtrl--SetColumnOrderArray.md)