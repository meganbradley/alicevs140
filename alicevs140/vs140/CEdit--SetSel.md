---
title: "CEdit::SetSel"
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
ms.assetid: 5ea37afd-9325-4fc6-967d-27b7d7bddf1d
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CEdit::SetSel
Call this function to select a range of characters in an edit control.  
  
## Syntax  
  
```  
  
      void SetSel(  
   DWORD dwSelection,  
   BOOL bNoScroll = FALSE   
);  
void SetSel(  
   int nStartChar,  
   int nEndChar,  
   BOOL bNoScroll = FALSE   
);  
```  
  
#### Parameters  
 *dwSelection*  
 Specifies the starting position in the low-order word and the ending position in the high-order word. If the low-order word is 0 and the high-order word is –1, all the text in the edit control is selected. If the low-order word is –1, any current selection is removed.  
  
 *bNoScroll*  
 Indicates whether the caret should be scrolled into view. If **FALSE**, the caret is scrolled into view. If **TRUE**, the caret is not scrolled into view.  
  
 `nStartChar`  
 Specifies the starting position. If `nStartChar` is 0 and `nEndChar` is –1, all the text in the edit control is selected. If `nStartChar` is –1, any current selection is removed.  
  
 `nEndChar`  
 Specifies the ending position.  
  
## Remarks  
 For more information, see [EM_SETSEL](http://msdn.microsoft.com/library/windows/desktop/bb761661) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 See the example for [CEdit::GetSel](../vs140/CEdit--GetSel.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CEdit Class](../vs140/CEdit-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CEdit::GetSel](../vs140/CEdit--GetSel.md)   
 [CEdit::ReplaceSel](../vs140/CEdit--ReplaceSel.md)