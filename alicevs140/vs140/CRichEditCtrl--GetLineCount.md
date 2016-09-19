---
title: "CRichEditCtrl::GetLineCount"
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
ms.assetid: 8bdb0797-885e-4796-8adf-fb0a57b73d39
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditCtrl::GetLineCount
Retrieves the number of lines in the `CRichEditCtrl` object.  
  
## Syntax  
  
```  
  
int GetLineCount( ) const;  
  
```  
  
## Return Value  
 The number of lines in this `CRichEditCtrl` object.  
  
## Remarks  
 For more information, see [EM_GETLINECOUNT](http://msdn.microsoft.com/library/windows/desktop/bb761586) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CRichEditCtrl#13](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CRichEditCtrl#13)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CRichEditCtrl Class](../vs140/CRichEditCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditCtrl::GetLine](../vs140/CRichEditCtrl--GetLine.md)