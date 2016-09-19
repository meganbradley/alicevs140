---
title: "CFindReplaceDialog::GetFindString"
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
ms.assetid: 9bc5d133-d41a-44e2-8a08-56989afd53e2
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFindReplaceDialog::GetFindString
Call this function from your callback function to retrieve the default string to find.  
  
## Syntax  
  
```  
  
CString GetFindString( ) const;  
```  
  
## Return Value  
 The default string to find.  
  
## Example  
 [!CODE [NVC_MFCDocView#69](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#69)]  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CFindReplaceDialog Class](../vs140/CFindReplaceDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFindReplaceDialog::FindNext](../vs140/CFindReplaceDialog--FindNext.md)   
 [CFindReplaceDialog::GetReplaceString](../vs140/CFindReplaceDialog--GetReplaceString.md)