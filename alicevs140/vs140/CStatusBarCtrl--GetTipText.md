---
title: "CStatusBarCtrl::GetTipText"
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
ms.assetid: 36d456ff-66e3-4930-abb5-04011a3763de
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStatusBarCtrl::GetTipText
Retrieves the tooltip text for a pane in a status bar.  
  
## Syntax  
  
```  
  
      CString GetTipText(  
   int nPane   
) const;  
```  
  
#### Parameters  
 `nPane`  
 The zero-based index of status bar pane to receive the tooltip text.  
  
## Return Value  
 A [CString](../vs140/CStringT-Class.md) object containing the text to be used in the tooltip.  
  
## Remarks  
 This member function implements the behavior of the Win32 message [SB_GETTIPTEXT](http://msdn.microsoft.com/library/windows/desktop/bb760751), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CStatusBarCtrl#7](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CStatusBarCtrl#7)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CStatusBar Class](../vs140/CStatusBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CStatusBarCtrl::SetTipText](../vs140/CStatusBarCtrl--SetTipText.md)