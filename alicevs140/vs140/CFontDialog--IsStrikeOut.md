---
title: "CFontDialog::IsStrikeOut"
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
ms.assetid: fa1e3a68-f1a9-40e1-a0f2-19fdea2bff52
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFontDialog::IsStrikeOut
Call this function to determine if the selected font is displayed with strikeout.  
  
## Syntax  
  
```  
  
BOOL IsStrikeOut( ) const;  
```  
  
## Return Value  
 Nonzero if the selected font has the Strikeout characteristic enabled; otherwise 0.  
  
## Example  
 [!CODE [NVC_MFCDocView#87](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#87)]  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CFontDialog Class](../vs140/CFontDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFontDialog::GetCurrentFont](../vs140/CFontDialog--GetCurrentFont.md)