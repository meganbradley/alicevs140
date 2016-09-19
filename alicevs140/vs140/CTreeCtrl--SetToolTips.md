---
title: "CTreeCtrl::SetToolTips"
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
ms.assetid: 23980b3b-09cc-4b78-8efa-0eb0d4c13a18
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTreeCtrl::SetToolTips
This member function implements the behavior of the Win32 message [TVM_SETTOOLTIPS](http://msdn.microsoft.com/library/windows/desktop/bb773772), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Syntax  
  
```  
  
      CToolTipCtrl* SetToolTips(  
   CToolTipCtrl* pWndTip   
);  
```  
  
#### Parameters  
 `pWndTip`  
 A pointer to a [CToolTipCtrl](../vs140/CToolTipCtrl-Class.md) object that the tree control will use.  
  
## Return Value  
 A pointer to a [CToolTipCtrl](../vs140/CToolTipCtrl-Class.md) object containing the tooltip previously used by the control, or **NULL** if no tooltips were used previously.  
  
## Remarks  
 To use tooltips, indicate the **TVS_NOTOOLTIPS** style when you create the `CTreeCtrl` object.  
  
## Example  
 See the example for [CTreeCtrl::GetToolTips](../vs140/CTreeCtrl--GetToolTips.md).  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CTreeCtrl Class](../vs140/CTreeCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTreeCtrl::GetToolTips](../vs140/CTreeCtrl--GetToolTips.md)   
 [CTreeCtrl::Create](../vs140/CTreeCtrl--Create.md)