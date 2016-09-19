---
title: "CRichEditCtrl::Clear"
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
ms.assetid: 4fe696b7-d67b-4838-88de-1f678a415901
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditCtrl::Clear
Deletes (clears) the current selection (if any) in the rich edit control.  
  
## Syntax  
  
```  
  
void Clear( );  
  
```  
  
## Remarks  
 The deletion performed by **Clear** can be undone by calling the [Undo](../vs140/CRichEditCtrl--Undo.md) member function.  
  
 To delete the current selection and place the deleted contents onto the Clipboard, call the [Cut](../vs140/CRichEditCtrl--Cut.md) member function.  
  
 For more information, see [WM_CLEAR](http://msdn.microsoft.com/library/windows/desktop/ms649020) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CRichEditCtrl#3](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CRichEditCtrl#3)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CRichEditCtrl Class](../vs140/CRichEditCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditCtrl::Undo](../vs140/CRichEditCtrl--Undo.md)   
 [CRichEditCtrl::Cut](../vs140/CRichEditCtrl--Cut.md)   
 [CRichEditCtrl::Copy](../vs140/CRichEditCtrl--Copy.md)   
 [CRichEditCtrl::Paste](../vs140/CRichEditCtrl--Paste.md)