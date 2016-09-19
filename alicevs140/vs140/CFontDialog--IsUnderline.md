---
title: "CFontDialog::IsUnderline"
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
ms.assetid: 68d3979d-6e97-4bae-8ee0-89f62315c0c3
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFontDialog::IsUnderline
Call this function to determine if the selected font is underlined.  
  
## Syntax  
  
```  
  
BOOL IsUnderline( ) const;  
```  
  
## Return Value  
 Nonzero if the selected font has the Underline characteristic enabled; otherwise 0.  
  
## Example  
 [!CODE [NVC_MFCDocView#88](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#88)]  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CFontDialog Class](../vs140/CFontDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFontDialog::GetCurrentFont](../vs140/CFontDialog--GetCurrentFont.md)