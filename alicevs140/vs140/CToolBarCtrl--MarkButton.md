---
title: "CToolBarCtrl::MarkButton"
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
ms.assetid: 7599854f-7769-407c-9d2e-c841bc53e1bb
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolBarCtrl::MarkButton
Sets the highlight state of a given button in a toolbar control.  
  
## Syntax  
  
```  
  
      BOOL MarkButton(  
   int nID,  
   BOOL fHighlight = TRUE   
);  
```  
  
#### Parameters  
 `nID`  
 The button identifier.  
  
 `fHighlight`  
 Specifies the highlight state to be set. By default, **TRUE**. If set to **FALSE**, the button is set to its default state.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 This member function implements the behavior of the Win32 message [TB_MARKBUTTON](http://msdn.microsoft.com/library/windows/desktop/bb787385), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CToolBarCtrl Class](../vs140/CToolBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CToolBarCtrl::IsButtonHighlighted](../vs140/CToolBarCtrl--IsButtonHighlighted.md)