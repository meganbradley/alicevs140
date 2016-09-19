---
title: "CFontDialog::GetWeight"
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
ms.assetid: 43d6f359-160a-42f6-8c02-41007fbfa5e1
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFontDialog::GetWeight
Call this function to retrieve the weight of the selected font.  
  
## Syntax  
  
```  
  
int GetWeight( ) const;  
```  
  
## Return Value  
 The weight of the selected font.  
  
## Remarks  
 For more information on the weight of a font, see [CFont::CreateFont](../vs140/CFont--CreateFont.md).  
  
## Example  
 [!CODE [NVC_MFCDocView#84](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#84)]  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CFontDialog Class](../vs140/CFontDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFontDialog::GetCurrentFont](../vs140/CFontDialog--GetCurrentFont.md)   
 [CFontDialog::IsBold](../vs140/CFontDialog--IsBold.md)