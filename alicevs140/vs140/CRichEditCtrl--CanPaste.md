---
title: "CRichEditCtrl::CanPaste"
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
ms.assetid: 7e3f709d-ccf1-46ec-9c81-e5b006b42f1f
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditCtrl::CanPaste
Determines if the rich edit control can paste the specified Clipboard format.  
  
## Syntax  
  
```  
  
      BOOL CanPaste(  
   UINT nFormat = 0   
) const;  
```  
  
#### Parameters  
 `nFormat`  
 The Clipboard data format to query. This parameter can be one of the predefined Clipboard formats or the value returned by [RegisterClipboardFormat](http://msdn.microsoft.com/library/windows/desktop/ms649049).  
  
## Return Value  
 Nonzero if the Clipboard format can be pasted; otherwise 0.  
  
## Remarks  
 If `nFormat` is 0, `CanPaste` will try any format currently on the Clipboard.  
  
 For more information, see [EM_CANPASTE](http://msdn.microsoft.com/library/windows/desktop/bb787993) message and [RegisterClipboardFormat](http://msdn.microsoft.com/library/windows/desktop/ms649049) function in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CRichEditCtrl#1](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CRichEditCtrl#1)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CRichEditCtrl Class](../vs140/CRichEditCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditCtrl::Paste](../vs140/CRichEditCtrl--Paste.md)   
 [CRichEditCtrl::PasteSpecial](../vs140/CRichEditCtrl--PasteSpecial.md)