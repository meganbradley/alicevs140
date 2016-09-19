---
title: "CListCtrl::SetIconSpacing"
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
ms.assetid: cd803b6d-5231-4a9c-a525-9d18370a30d0
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::SetIconSpacing
Sets the spacing between icons in a list view control.  
  
## Syntax  
  
```  
  
      CSize SetIconSpacing(  
   int cx,  
   int cy   
);  
CSize SetIconSpacing(  
   CSize size   
);  
```  
  
#### Parameters  
 `cx`  
 The distance (in pixels) between icons on the x-axis.  
  
 `cy`  
 The distance (in pixels) between icons on the y-axis.  
  
 `size`  
 A `CSize` object specifying the distance (in pixels) between icons on the x- and y-axes.  
  
## Return Value  
 A [CSize](../vs140/CSize-Class.md) object containing the previous values for icon spacing.  
  
## Remarks  
 This member function implements the behavior of the Win32 macro, [ListView_SetIconSpacing](http://msdn.microsoft.com/library/windows/desktop/bb775085), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CListCtrl#34](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListCtrl#34)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)