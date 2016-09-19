---
title: "CPrintDialog::PrintCollate"
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
ms.assetid: b6c40861-5f1e-42a3-868b-1d2c33de5f9e
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPrintDialog::PrintCollate
Determines whether collated copies are requested.  
  
## Syntax  
  
```  
  
BOOL PrintCollate( ) const;  
```  
  
## Return Value  
 Nonzero if the user selects the collate check box in the dialog box; otherwise 0.  
  
## Remarks  
 Call this function after calling `DoModal` to determine whether the printer should collate all printed copies of the document.  
  
## Example  
 [!CODE [NVC_MFCDocView#110](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#110)]  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CPrintDialog Class](../vs140/CPrintDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPrintDialog::GetCopies](../vs140/CPrintDialog--GetCopies.md)