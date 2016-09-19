---
title: "CEdit::Copy"
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
ms.assetid: dccd7d20-6968-4328-b41e-c155120a2282
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CEdit::Copy
Call this function to coy the current selection (if any) in the edit control to the Clipboard in **CF_TEXT** format.  
  
## Syntax  
  
```  
  
void Copy( );  
```  
  
## Remarks  
 For more information, see [WM_COPY](http://msdn.microsoft.com/library/windows/desktop/ms649022) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CEdit#5](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CEdit#5)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CEdit Class](../vs140/CEdit-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CEdit::Clear](../vs140/CEdit--Clear.md)   
 [CEdit::Cut](../vs140/CEdit--Cut.md)   
 [CEdit::Paste](../vs140/CEdit--Paste.md)