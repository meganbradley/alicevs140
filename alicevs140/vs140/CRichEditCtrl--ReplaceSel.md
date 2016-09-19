---
title: "CRichEditCtrl::ReplaceSel"
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
ms.assetid: 9e27db0d-a46f-4479-8328-36f7ea1bbf18
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditCtrl::ReplaceSel
Replaces the current selection in this `CRichEditCtrl` object with the specified text.  
  
## Syntax  
  
```  
  
      void ReplaceSel(  
   LPCTSTR lpszNewText,  
   BOOL bCanUndo = FALSE   
);  
```  
  
#### Parameters  
 `lpszNewText`  
 Pointer to a null-terminated string containing the replacement text.  
  
 `bCanUndo`  
 To specify that this function can be undone, set the value of this parameter to **TRUE**. The default value is **FALSE**.  
  
## Remarks  
 To replace all the text in this `CRichEditCtrl` object, use [CWnd::SetWindowText](../vs140/CWnd--SetWindowText.md).  
  
 If there is no current selection, the replacement text is inserted at the insertion point, that is, the current caret location.  
  
 This function will format the inserted text with the existing character formatting. When replacing the entire range of text (by calling `SetSel`(0,-1) before calling `ReplaceSel`), there is an end of paragraph character that retains the previous paragraph's formatting, which in inherited by the newly inserted text.  
  
 For more information, see [EM_REPLACESEL](http://msdn.microsoft.com/library/windows/desktop/bb761633) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 See the example for [LineIndex](../vs140/CRichEditCtrl--LineIndex.md).  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CRichEditCtrl Class](../vs140/CRichEditCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditCtrl::CanUndo](../vs140/CRichEditCtrl--CanUndo.md)   
 [CRichEditCtrl::Undo](../vs140/CRichEditCtrl--Undo.md)   
 [CWnd::SetWindowText](../vs140/CWnd--SetWindowText.md)