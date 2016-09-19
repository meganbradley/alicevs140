---
title: "CStatusBarCtrl::SetText"
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
ms.assetid: 92ece860-8cfd-467a-9213-fc59dff5ed14
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStatusBarCtrl::SetText
Sets the text in the given part of a status bar control.  
  
## Syntax  
  
```  
  
      BOOL SetText(  
   LPCTSTR lpszText,  
   int nPane,  
   int nType   
);  
```  
  
#### Parameters  
 `lpszText`  
 Address of a null-terminated string specifying the text to set. If `nType` is `SBT_OWNERDRAW`, `lpszText` represents 32 bits of data.  
  
 `nPane`  
 Zero-based index of the part to set. If this value is 255, the status bar control is assumed to be a simple control having only one part.  
  
 `nType`  
 Type of drawing operation. See [SB_SETTEXT message](http://msdn.microsoft.com/library/bb760758\(VS.85\).aspx) for a list of possible values.  
  
## Return Value  
 Nonzero if successful; otherwise zero.  
  
## Remarks  
 The message invalidates the portion of the control that has changed, causing it to display the new text when the control next receives the `WM_PAINT` message.  
  
## Example  
 [!CODE [NVC_MFC_CStatusBarCtrl#11](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CStatusBarCtrl#11)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CStatusBarCtrl Class](../vs140/CStatusBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CStatusBarCtrl::GetText](../vs140/CStatusBarCtrl--GetText.md)   
 [CStatusBarCtrl::GetTextLength](../vs140/CStatusBarCtrl--GetTextLength.md)