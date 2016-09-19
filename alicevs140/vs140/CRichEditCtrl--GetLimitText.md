---
title: "CRichEditCtrl::GetLimitText"
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
ms.assetid: f2b960a1-60b2-48b5-aa5b-cfb919aaccf8
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditCtrl::GetLimitText
Gets the text limit for this `CRichEditCtrl` object.  
  
## Syntax  
  
```  
  
long GetLimitText( ) const;  
  
```  
  
## Return Value  
 The current text limit, in bytes, for this `CRichEditCtrl` object.  
  
## Remarks  
 The text limit is the maximum amount of text, in bytes, the rich edit control can accept.  
  
 For more information, see [EM_GETLIMITTEXT](http://msdn.microsoft.com/library/windows/desktop/bb761582) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CRichEditCtrl#12](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CRichEditCtrl#12)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CRichEditCtrl Class](../vs140/CRichEditCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditCtrl::LimitText](../vs140/CRichEditCtrl--LimitText.md)