---
title: "CRichEditView::AdjustDialogPosition"
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
ms.assetid: e6890a9e-1416-46d0-b577-3f83aee9a7c6
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditView::AdjustDialogPosition
Call this function to move the given dialog box so that it does not obscure the current selection.  
  
## Syntax  
  
```  
  
      void AdjustDialogPosition(  
   CDialog* pDlg   
);  
```  
  
#### Parameters  
 *pDlg*  
 Pointer to a `CDialog` object.  
  
## Requirements  
 **Header:** afxrich.h  
  
## See Also  
 [CRichEditView Class](../vs140/CRichEditView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditCtrl::GetSel](../vs140/CRichEditCtrl--GetSel.md)