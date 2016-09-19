---
title: "CListCtrl::SetExtendedStyle"
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
ms.assetid: 48dc8493-ff96-4966-a973-858fa5d97745
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::SetExtendedStyle
Sets the current extended styles of a list view control.  
  
## Syntax  
  
```  
  
      DWORD SetExtendedStyle(  
   DWORD dwNewStyle   
);  
```  
  
#### Parameters  
 `dwNewStyle`  
 A combination of extended styles to be used by the list view control. For a descriptive list of these styles, see the [Extended List View Styles](http://msdn.microsoft.com/library/windows/desktop/bb774732) topic in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Return Value  
 A combination of the previous extended styles used by the list view control.  
  
## Remarks  
 This member function implements the behavior of the Win32 macro, [ListView_SetExtendedListViewStyle](http://msdn.microsoft.com/library/windows/desktop/bb775076), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CListCtrl#16](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListCtrl#16)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListCtrl::CreateEx](../vs140/CListCtrl--CreateEx.md)   
 [CListCtrl::GetExtendedStyle](../vs140/CListCtrl--GetExtendedStyle.md)