---
title: "CFontDialog::GetColor"
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
ms.assetid: 8461e57e-d10d-43b2-b5c6-bba4a6276d1b
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFontDialog::GetColor
Call this function to retrieve the selected font color.  
  
## Syntax  
  
```  
  
COLORREF GetColor( ) const;  
```  
  
## Return Value  
 The color of the selected font.  
  
## Example  
 [!CODE [NVC_MFCDocView#79](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#79)]  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CFontDialog Class](../vs140/CFontDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFontDialog::GetCurrentFont](../vs140/CFontDialog--GetCurrentFont.md)