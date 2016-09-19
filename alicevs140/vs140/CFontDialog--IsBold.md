---
title: "CFontDialog::IsBold"
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
ms.assetid: c289c692-3f84-4ded-a456-4ee3e2f016f4
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFontDialog::IsBold
Call this function to determine if the selected font is bold.  
  
## Syntax  
  
```  
  
BOOL IsBold( ) const;  
```  
  
## Return Value  
 Nonzero if the selected font has the Bold characteristic enabled; otherwise 0.  
  
## Example  
 [!CODE [NVC_MFCDocView#85](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#85)]  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CFontDialog Class](../vs140/CFontDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFontDialog::GetCurrentFont](../vs140/CFontDialog--GetCurrentFont.md)