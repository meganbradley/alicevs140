---
title: "CToolBarCtrl::GetAnchorHighlight"
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
ms.assetid: 58b56c7d-406f-4d9b-9233-035ead10ded1
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolBarCtrl::GetAnchorHighlight
Retrieves the anchor highlight setting for a toolbar.  
  
## Syntax  
  
```  
  
BOOL GetAnchorHighlight( ) const;  
  
```  
  
## Return Value  
 If nonzero, anchor highlighting is enabled. If zero, anchor highlighting is disabled.  
  
## Remarks  
 This member function implements the behavior of the Win32 message [TB_GETANCHORHIGHLIGHT](http://msdn.microsoft.com/library/windows/desktop/bb787313), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CToolBarCtrl Class](../vs140/CToolBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CToolBarCtrl::SetAnchorHighlight](../vs140/CToolBarCtrl--SetAnchorHighlight.md)