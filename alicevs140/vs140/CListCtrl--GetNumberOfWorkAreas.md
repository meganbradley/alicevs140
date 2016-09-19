---
title: "CListCtrl::GetNumberOfWorkAreas"
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
ms.assetid: d227009f-25c7-4959-9709-2294b3d90013
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::GetNumberOfWorkAreas
Retrieves the current number of working areas for a list view control.  
  
## Syntax  
  
```  
  
UINT GetNumberOfWorkAreas( ) const;  
  
```  
  
## Return Value  
 Not used at this time.  
  
## Remarks  
 This member function implements the behavior of the Win32 macro, [ListView_GetNumberOfWorkAreas](http://msdn.microsoft.com/library/windows/desktop/bb774988), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CListCtrl#25](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListCtrl#25)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListCtrl::GetWorkAreas](../vs140/CListCtrl--GetWorkAreas.md)