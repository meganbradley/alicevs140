---
title: "CRichEditCtrl::EmptyUndoBuffer"
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
ms.assetid: c319bbb3-6606-450a-9d42-11afcf282c2e
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditCtrl::EmptyUndoBuffer
Resets (clear) the undo flag of this rich edit control.  
  
## Syntax  
  
```  
  
void EmptyUndoBuffer( );  
  
```  
  
## Remarks  
 The control will now be unable to undo the last editing operation. The undo flag is set whenever an operation within the rich edit control can be undone.  
  
 The undo flag is automatically cleared whenever you call the [CWnd](../vs140/CWnd-Class.md) member function [SetWindowText](../vs140/CWnd--SetWindowText.md).  
  
 For more information, see [EM_EMPTYUNDOBUFFER](http://msdn.microsoft.com/library/windows/desktop/bb761568) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CRichEditCtrl#8](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CRichEditCtrl#8)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CRichEditCtrl Class](../vs140/CRichEditCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditCtrl::CanUndo](../vs140/CRichEditCtrl--CanUndo.md)   
 [CRichEditCtrl::Undo](../vs140/CRichEditCtrl--Undo.md)   
 [CWnd::SetWindowText](../vs140/CWnd--SetWindowText.md)