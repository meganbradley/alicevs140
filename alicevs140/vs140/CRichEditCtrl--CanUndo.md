---
title: "CRichEditCtrl::CanUndo"
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
ms.assetid: 809f2f22-2557-4821-aebd-f4d4e7134500
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditCtrl::CanUndo
Determines if the last editing operation can be undone.  
  
## Syntax  
  
```  
  
BOOL CanUndo( ) const;  
  
```  
  
## Return Value  
 Nonzero if the last edit operation can be undone by a call to the [Undo](../vs140/CRichEditCtrl--Undo.md) member function; 0 if it cannot be undone.  
  
## Remarks  
 For more information, see [EM_CANUNDO](http://msdn.microsoft.com/library/windows/desktop/bb775468) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CRichEditCtrl#2](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CRichEditCtrl#2)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CRichEditCtrl Class](../vs140/CRichEditCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditCtrl::Undo](../vs140/CRichEditCtrl--Undo.md)   
 [CRichEditCtrl::EmptyUndoBuffer](../vs140/CRichEditCtrl--EmptyUndoBuffer.md)   
 [CRichEditCtrl::CanRedo](../vs140/CRichEditCtrl--CanRedo.md)   
 [CRichEditCtrl::GetRedoName](../vs140/CRichEditCtrl--GetRedoName.md)