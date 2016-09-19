---
title: "CStatusBarCtrl::SetBkColor"
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
ms.assetid: 9fddbd97-f531-4f43-8d8d-f5ac30b8e3ad
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStatusBarCtrl::SetBkColor
Sets the background color in a status bar.  
  
## Syntax  
  
```  
  
      COLORREF SetBkColor(  
   COLORREF cr   
);  
```  
  
#### Parameters  
 `cr`  
 **COLORREF** value that specifies the new background color. Specify the `CLR_DEFAULT` value to cause the status bar to use its default background color.  
  
## Return Value  
 A [COLORREF](http://msdn.microsoft.com/library/windows/desktop/dd183449) value that represents the previous default background color.  
  
## Remarks  
 This member function implements the behavior of the Win32 message [SB_SETBKCOLOR](http://msdn.microsoft.com/library/windows/desktop/bb760754), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CStatusBarCtrl#8](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CStatusBarCtrl#8)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CStatusBar Class](../vs140/CStatusBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)