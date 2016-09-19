---
title: "CTreeCtrl::GetToolTips"
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
ms.assetid: d1c95b8c-2492-4d89-9ba2-41147f72cf96
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTreeCtrl::GetToolTips
This member function implements the behavior of the Win32 message [TVM_GETTOOLTIPS](http://msdn.microsoft.com/library/windows/desktop/bb773729), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Syntax  
  
```  
  
CToolTipCtrl* GetToolTips( ) const;  
  
```  
  
## Return Value  
 A pointer to a [CToolTipCtrl](../vs140/CToolTipCtrl-Class.md) object to be used by the tree control. If the [Create](../vs140/CTreeCtrl--Create.md) member function uses the style **TVS_NOTOOLTIPS**, no tooltips are used, and **NULL** is returned.  
  
## Remarks  
 The MFC implementation of `GetToolTips` returns a `CToolTipCtrl` object, which is used by the tree control, rather than a handle to a tooltip control.  
  
## Example  
 [!CODE [NVC_MFC_CTreeCtrl#25](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CTreeCtrl#25)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CTreeCtrl Class](../vs140/CTreeCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTreeCtrl::SetToolTips](../vs140/CTreeCtrl--SetToolTips.md)