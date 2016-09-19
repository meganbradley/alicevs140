---
title: "CEdit::Cut"
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
ms.assetid: 237e5632-9328-4dbf-bbdd-7ef4af0cdf21
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CEdit::Cut
Call this function to delete (cut) the current selection (if any) in the edit control and copy the deleted text to the Clipboard in **CF_TEXT** format.  
  
## Syntax  
  
```  
  
void Cut( );  
```  
  
## Remarks  
 The deletion performed by **Cut** can be undone by calling the [Undo](../vs140/CEdit--Undo.md) member function.  
  
 To delete the current selection without placing the deleted text into the Clipboard, call the [Clear](../vs140/CEdit--Clear.md) member function.  
  
 For more information, see [WM_CUT](http://msdn.microsoft.com/library/windows/desktop/ms649023) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CEdit#6](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CEdit#6)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CEdit Class](../vs140/CEdit-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CEdit::Undo](../vs140/CEdit--Undo.md)   
 [CEdit::Clear](../vs140/CEdit--Clear.md)   
 [CEdit::Copy](../vs140/CEdit--Copy.md)   
 [CEdit::Paste](../vs140/CEdit--Paste.md)