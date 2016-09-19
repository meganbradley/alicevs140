---
title: "CRichEditCtrl::Undo"
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
ms.assetid: 66e8832b-b48d-4c3d-a1fb-3933b842f3fb
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditCtrl::Undo
Undoes the last operation in the rich edit control.  
  
## Syntax  
  
```  
  
BOOL Undo( );  
  
```  
  
## Return Value  
 Nonzero if the undo operation is successful; otherwise, 0.  
  
## Remarks  
 An undo operation can also be undone. For example, you can restore deleted text with the first call to **Undo**. As long as there is no intervening edit operation, you can remove the text again with a second call to **Undo**.  
  
 For more information, see [EM_UNDO](http://msdn.microsoft.com/library/windows/desktop/bb761670) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 See the example for [CanUndo](../vs140/CRichEditCtrl--CanUndo.md).  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CRichEditCtrl Class](../vs140/CRichEditCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditCtrl::CanUndo](../vs140/CRichEditCtrl--CanUndo.md)   
 [CRichEditCtrl::EmptyUndoBuffer](../vs140/CRichEditCtrl--EmptyUndoBuffer.md)