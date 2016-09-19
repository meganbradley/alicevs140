---
title: "CToolTipCtrl::SetMargin"
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
ms.assetid: 7217236d-5712-4bc1-8f69-5f700debe4e1
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolTipCtrl::SetMargin
Sets the top, left, bottom, and right margins for a tool tip window.  
  
## Syntax  
  
```  
  
      void SetMargin(  
   LPRECT lprc   
);  
```  
  
#### Parameters  
 `lprc`  
 Address of a `RECT` structure that contains the margin information to be set. The members of the `RECT` structure do not define a bounding rectangle. See [CToolTipCtrl::GetMargin](../vs140/CToolTipCtrl--GetMargin.md) for a description of the margin information.  
  
## Remarks  
 This member function implements the behavior of the Win32 message [TTM_SETMARGIN](http://msdn.microsoft.com/library/windows/desktop/bb760406), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CToolTipCtrl Class](../vs140/CToolTipCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CToolTipCtrl::GetMargin](../vs140/CToolTipCtrl--GetMargin.md)