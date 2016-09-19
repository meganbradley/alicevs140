---
title: "CEdit::Clear"
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
ms.assetid: ec508beb-b9c5-4fe1-b7e2-10e6c27a802b
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CEdit::Clear
Call this function to delete (clear) the current selection (if any) in the edit control.  
  
## Syntax  
  
```  
  
void Clear( );  
```  
  
## Remarks  
 The deletion performed by **Clear** can be undone by calling the [Undo](../vs140/CEdit--Undo.md) member function.  
  
 To delete the current selection and place the deleted contents into the Clipboard, call the [Cut](../vs140/CEdit--Cut.md) member function.  
  
 For more information, see [WM_CLEAR](http://msdn.microsoft.com/library/windows/desktop/ms649020) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CEdit#4](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CEdit#4)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CEdit Class](../vs140/CEdit-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CEdit::Undo](../vs140/CEdit--Undo.md)   
 [CEdit::Copy](../vs140/CEdit--Copy.md)   
 [CEdit::Cut](../vs140/CEdit--Cut.md)   
 [CEdit::Paste](../vs140/CEdit--Paste.md)