---
title: "CRichEditView::FindTextSimple"
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
ms.assetid: 4b8afdbe-26ba-4713-bbef-86e86f7b1836
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditView::FindTextSimple
Call this function to find the specified text and set it to be the current selection.  
  
## Syntax  
  
```  
  
      BOOL FindTextSimple(  
   LPCTSTR lpszFind,  
   BOOL bCase = TRUE,  
   BOOL bWord = TRUE,  
   BOOL bNext = TRUE   
);  
```  
  
#### Parameters  
 `lpszFind`  
 Contains the string to search for.  
  
 `bCase`  
 Indicates if the search is case sensitive.  
  
 `bWord`  
 Indicates if the search should match whole words only, not parts of words.  
  
 `bNext`  
 Indicates the direction of the search. If **TRUE**, the search direction is toward the end of the buffer. If **FALSE**, the search direction is toward the beginning of the buffer.  
  
## Return Value  
 Nonzero if the `lpszFind` text is found; otherwise 0.  
  
## Example  
 See the example for [CRichEditView::FindText](../vs140/CRichEditView--FindText.md).  
  
## Requirements  
 **Header:** afxrich.h  
  
## See Also  
 [CRichEditView Class](../vs140/CRichEditView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditCtrl::FindText](../vs140/CRichEditCtrl--FindText.md)   
 [CRichEditCtrl::SetSel](../vs140/CRichEditCtrl--SetSel.md)   
 [CRichEditView::FindText](../vs140/CRichEditView--FindText.md)