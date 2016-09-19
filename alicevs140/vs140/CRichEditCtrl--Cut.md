---
title: "CRichEditCtrl::Cut"
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
ms.assetid: ac84099b-dcdb-42ff-aff6-4e688d6807b7
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditCtrl::Cut
Delete (cuts) the current selection (if any) in the rich edit control and copies the deleted text to the Clipboard.  
  
## Syntax  
  
```  
  
void Cut( );  
  
```  
  
## Remarks  
 The deletion performed by **Cut** can be undone by calling the [Undo](../vs140/CRichEditCtrl--Undo.md) member function.  
  
 To delete the current selection without placing the deleted text into the Clipboard, call the [Clear](../vs140/CRichEditCtrl--Clear.md) member function.  
  
 For more information, see [WM_CUT](http://msdn.microsoft.com/library/windows/desktop/ms649023) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CRichEditCtrl#7](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CRichEditCtrl#7)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CRichEditCtrl Class](../vs140/CRichEditCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditCtrl::Copy](../vs140/CRichEditCtrl--Copy.md)   
 [CRichEditCtrl::Undo](../vs140/CRichEditCtrl--Undo.md)   
 [CRichEditCtrl::Clear](../vs140/CRichEditCtrl--Clear.md)