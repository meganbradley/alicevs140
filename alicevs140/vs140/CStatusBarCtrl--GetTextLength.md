---
title: "CStatusBarCtrl::GetTextLength"
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
ms.assetid: d9e0b7c5-1180-45a1-b660-2b56a67be4a8
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStatusBarCtrl::GetTextLength
Retrieves the length, in characters, of the text from the given part of a status bar control.  
  
## Syntax  
  
```  
  
      int GetTextLength(  
   int nPane,  
   int* pType = NULL  
) const;  
```  
  
#### Parameters  
 `nPane`  
 Zero-based index of the part from which to retrieve text.  
  
 `pType`  
 Pointer to an integer that receives the type information. The type can be one of these values:  
  
-   **0** The text is drawn with a border to appear lower than the plane of the status bar.  
  
-   `SBT_NOBORDERS` The text is drawn without borders.  
  
-   `SBT_OWNERDRAW` The text is drawn by the parent window.  
  
-   `SBT_POPOUT` The text is drawn with a border to appear higher than the plane of the status bar.  
  
## Return Value  
 The length, in characters, of the text.  
  
## Example  
 [!CODE [NVC_MFC_CStatusBarCtrl#6](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CStatusBarCtrl#6)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CStatusBarCtrl Class](../vs140/CStatusBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CStatusBarCtrl::GetText](../vs140/CStatusBarCtrl--GetText.md)   
 [CStatusBarCtrl::SetText](../vs140/CStatusBarCtrl--SetText.md)