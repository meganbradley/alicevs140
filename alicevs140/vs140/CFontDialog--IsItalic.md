---
title: "CFontDialog::IsItalic"
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
ms.assetid: d1b10398-73ae-4b63-9cd3-477e68a028e6
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFontDialog::IsItalic
Call this function to determine if the selected font is italic.  
  
## Syntax  
  
```  
  
BOOL IsItalic( ) const;  
```  
  
## Return Value  
 Nonzero if the selected font has the Italic characteristic enabled; otherwise 0.  
  
## Example  
 [!CODE [NVC_MFCDocView#86](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#86)]  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CFontDialog Class](../vs140/CFontDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFontDialog::GetCurrentFont](../vs140/CFontDialog--GetCurrentFont.md)