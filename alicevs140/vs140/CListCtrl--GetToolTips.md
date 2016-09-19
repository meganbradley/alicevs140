---
title: "CListCtrl::GetToolTips"
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
ms.assetid: 1627cdb2-a5c9-46bd-99c4-2c7a7637bf70
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::GetToolTips
Retrieves the tooltip control that the list view control uses to display tooltips.  
  
## Syntax  
  
```  
  
CToolTipCtrl* GetToolTips( ) const;  
  
```  
  
## Return Value  
 A pointer to a [CToolTipCtrl](../vs140/CToolTipCtrl-Class.md) object to be used by the list control. If the [Create](../vs140/CListCtrl--Create.md) member function uses the style **LVS_NOTOOLTIPS**, no tooltips are used, and **NULL** is returned.  
  
## Remarks  
 This member function implements the behavior of the Win32 message [LVM_GETTOOLTIPS](http://msdn.microsoft.com/library/windows/desktop/bb761085), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]. The MFC implementation of `GetToolTips` returns a `CToolTipCtrl` object, which is used by the list control, rather than a handle to a tooltip control.  
  
## Example  
 [!CODE [NVC_MFC_CListCtrl#29](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListCtrl#29)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListCtrl::SetToolTips](../vs140/CListCtrl--SetToolTips.md)