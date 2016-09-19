---
title: "CRichEditCtrl::GetTextLength"
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
ms.assetid: 453d3943-13df-4bc6-b52d-1d1168a726a3
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditCtrl::GetTextLength
Retrieves the length of the text, in characters, in this `CRichEditCtrl` object, not including the terminating null character.  
  
## Syntax  
  
```  
  
long GetTextLength( ) const;  
  
```  
  
## Return Value  
 The length of the text in this `CRichEditCtrl` object.  
  
## Remarks  
 For more information, see [WM_GETTEXTLENGTH](http://msdn.microsoft.com/library/windows/desktop/ms632628) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CRichEditCtrl#17](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CRichEditCtrl#17)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CRichEditCtrl Class](../vs140/CRichEditCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditCtrl::LimitText](../vs140/CRichEditCtrl--LimitText.md)   
 [CRichEditCtrl::GetLimitText](../vs140/CRichEditCtrl--GetLimitText.md)