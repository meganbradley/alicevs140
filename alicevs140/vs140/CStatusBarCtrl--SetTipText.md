---
title: "CStatusBarCtrl::SetTipText"
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
ms.assetid: 7505a1f3-0c37-4cb1-b30b-af83f75bdf91
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStatusBarCtrl::SetTipText
Sets the tooltip text for a pane in a status bar.  
  
## Syntax  
  
```  
  
      void SetTipText(  
   int nPane,  
   LPCTSTR pszTipText   
);  
```  
  
#### Parameters  
 `nPane`  
 The zero-based index of status bar pane to receive the tooltip text.  
  
 *pszTipText*  
 A pointer to a string containing the tooltip text.  
  
## Remarks  
 This member function implements the behavior of the Win32 message [SB_SETTIPTEXT](http://msdn.microsoft.com/library/windows/desktop/bb760759), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CStatusBarCtrl#12](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CStatusBarCtrl#12)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CStatusBar Class](../vs140/CStatusBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CStatusBarCtrl::GetTipText](../vs140/CStatusBarCtrl--GetTipText.md)