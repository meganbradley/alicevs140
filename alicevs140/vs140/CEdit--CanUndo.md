---
title: "CEdit::CanUndo"
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
ms.assetid: f8372005-7360-45aa-ad18-60ec2ce3b774
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CEdit::CanUndo
Call this function to determine if the last edit operation can be undone.  
  
## Syntax  
  
```  
  
BOOL CanUndo( ) const;  
```  
  
## Return Value  
 Nonzero if the last edit operation can be undone by a call to the **Undo** member function; 0 if it cannot be undone.  
  
## Remarks  
 For more information, see [EM_CANUNDO](http://msdn.microsoft.com/library/windows/desktop/bb775468) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 See the example for [CEdit::Undo](../vs140/CEdit--Undo.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CEdit Class](../vs140/CEdit-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CEdit::Undo](../vs140/CEdit--Undo.md)   
 [CEdit::EmptyUndoBuffer](../vs140/CEdit--EmptyUndoBuffer.md)