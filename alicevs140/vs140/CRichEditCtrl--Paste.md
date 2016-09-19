---
title: "CRichEditCtrl::Paste"
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
ms.assetid: 5b6c189a-fc3c-41e6-a648-807e6324b37a
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditCtrl::Paste
Inserts the data from the Clipboard into the `CRichEditCtrl` at the insertion point, the location of the caret.  
  
## Syntax  
  
```  
  
void Paste( );  
  
```  
  
## Remarks  
 Data is inserted only if the Clipboard contains data in a recognized format.  
  
 For more information, see [WM_PASTE](http://msdn.microsoft.com/library/windows/desktop/ms649028) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CRichEditCtrl#22](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CRichEditCtrl#22)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CRichEditCtrl Class](../vs140/CRichEditCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditCtrl::Copy](../vs140/CRichEditCtrl--Copy.md)   
 [CRichEditCtrl::Cut](../vs140/CRichEditCtrl--Cut.md)   
 [CRichEditCtrl::PasteSpecial](../vs140/CRichEditCtrl--PasteSpecial.md)