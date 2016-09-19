---
title: "CRichEditCtrl::Redo"
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
ms.assetid: 77005eab-1f42-4f1d-a240-56319b805df4
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditCtrl::Redo
Redoes the next action in the control's redo queue.  
  
## Syntax  
  
```  
  
BOOL Redo( );  
  
```  
  
## Return Value  
 Nonzero if successful; otherwise, 0.  
  
## Remarks  
 For more information, see [EM_REDO](http://msdn.microsoft.com/library/windows/desktop/bb774218) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CRichEditCtrl Class](../vs140/CRichEditCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditCtrl::Undo](../vs140/CRichEditCtrl--Undo.md)   
 [CRichEditCtrl::CanRedo](../vs140/CRichEditCtrl--CanRedo.md)   
 [CRichEditCtrl::GetRedoName](../vs140/CRichEditCtrl--GetRedoName.md)