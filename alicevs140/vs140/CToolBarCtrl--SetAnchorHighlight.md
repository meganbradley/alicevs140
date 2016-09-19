---
title: "CToolBarCtrl::SetAnchorHighlight"
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
ms.assetid: c149a710-c460-41f4-abda-679c7ce6a9be
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolBarCtrl::SetAnchorHighlight
Sets the anchor highlight setting for a toolbar.  
  
## Syntax  
  
```  
BOOL SetAnchorHighlight(  
   BOOL fAnchor = TRUE   
);  
```  
  
#### Parameters  
 [in] `fAnchor`  
 Specifies if anchor highlighting is enabled or disabled. If this value is nonzero, anchor highlighting will be enabled. If this value is zero, anchor highlighting will be disabled  
  
## Return Value  
 The previous anchor setting. If highlighting was enabled, this value is nonzero. If highlighting was not enabled, this value is zero.  
  
## Remarks  
 This method implements the behavior of the Win32 message [TB_SETANCHORHIGHLIGHT](http://msdn.microsoft.com/library/windows/desktop/bb787396), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CToolBarCtrl Class](../vs140/CToolBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CToolBarCtrl::GetAnchorHighlight](../vs140/CToolBarCtrl--GetAnchorHighlight.md)