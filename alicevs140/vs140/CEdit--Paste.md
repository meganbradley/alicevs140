---
title: "CEdit::Paste"
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
ms.assetid: 77e4ef92-3535-4025-9d2d-aa46ad41873a
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CEdit::Paste
Call this function to insert the data from the Clipboard into the `CEdit` at the insertion point.  
  
## Syntax  
  
```  
  
void Paste( );  
```  
  
## Remarks  
 Data is inserted only if the Clipboard contains data in **CF_TEXT** format.  
  
 For more information, see [WM_PASTE](http://msdn.microsoft.com/library/windows/desktop/ms649028) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CEdit#20](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CEdit#20)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CEdit Class](../vs140/CEdit-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CEdit::Clear](../vs140/CEdit--Clear.md)   
 [CEdit::Copy](../vs140/CEdit--Copy.md)   
 [CEdit::Cut](../vs140/CEdit--Cut.md)