---
title: "CListCtrl::SetWorkAreas"
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
ms.assetid: 18a0d19a-4379-4b38-ba70-86dd73b9d437
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::SetWorkAreas
Sets the area where icons can be displayed in a list view control.  
  
## Syntax  
  
```  
  
      void SetWorkAreas(  
   int nWorkAreas,  
   LPRECT lpRect   
);  
```  
  
#### Parameters  
 `nWorkAreas`  
 The number of `RECT` structures (or [CRect](../vs140/CRect-Class.md) objects) in the array pointed to by `lpRect`.  
  
 `lpRect`  
 The address of an array of `RECT` structures (or `CRect` objects) that specify the new work areas of the list view control. These areas must be specified in client coordinates. If this parameter is **NULL**, the working area will be set to the client area of the control.  
  
## Remarks  
 This member function implements the behavior of the Win32 macro, [ListView_SetWorkAreas](http://msdn.microsoft.com/library/windows/desktop/bb775128), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CListCtrl#39](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListCtrl#39)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)