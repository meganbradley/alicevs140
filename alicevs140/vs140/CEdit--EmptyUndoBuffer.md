---
title: "CEdit::EmptyUndoBuffer"
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
ms.assetid: 950ef09e-7253-40e3-b534-46bed631b747
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CEdit::EmptyUndoBuffer
Call this function to reset (clear) the undo flag of an edit control.  
  
## Syntax  
  
```  
  
void EmptyUndoBuffer( );  
```  
  
## Remarks  
 The edit control will now be unable to undo the last operation. The undo flag is set whenever an operation within the edit control can be undone.  
  
 The undo flag is automatically cleared whenever the [SetWindowText](../vs140/CWnd--SetWindowText.md) or [SetHandle](../vs140/CEdit--SetHandle.md) `CWnd` member functions are called.  
  
 For more information, see [EM_EMPTYUNDOBUFFER](http://msdn.microsoft.com/library/windows/desktop/bb761568) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CEdit#7](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CEdit#7)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CEdit Class](../vs140/CEdit-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CEdit::CanUndo](../vs140/CEdit--CanUndo.md)   
 [CEdit::SetHandle](../vs140/CEdit--SetHandle.md)   
 [CEdit::Undo](../vs140/CEdit--Undo.md)   
 [CWnd::SetWindowText](../vs140/CWnd--SetWindowText.md)