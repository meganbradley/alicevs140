---
title: "CFontDialog::GetFaceName"
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
ms.assetid: 50e745e0-31ea-4d34-b6c3-3736ae123a4d
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFontDialog::GetFaceName
Call this function to retrieve the face name of the selected font.  
  
## Syntax  
  
```  
  
CString GetFaceName( ) const;  
```  
  
## Return Value  
 The face name of the font selected in the `CFontDialog` dialog box.  
  
## Example  
 [!CODE [NVC_MFCDocView#81](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#81)]  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CFontDialog Class](../vs140/CFontDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFontDialog::GetCurrentFont](../vs140/CFontDialog--GetCurrentFont.md)   
 [CFontDialog::GetStyleName](../vs140/CFontDialog--GetStyleName.md)