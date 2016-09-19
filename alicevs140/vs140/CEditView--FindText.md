---
title: "CEditView::FindText"
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
ms.assetid: 143adf23-8490-4575-b962-f3a6fc991de7
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CEditView::FindText
Call the `FindText` function to search the `CEditView` object's text buffer.  
  
## Syntax  
  
```  
  
      BOOL FindText(  
   LPCTSTR lpszFind,  
   BOOL bNext = TRUE,  
   BOOL bCase = TRUE   
);  
```  
  
#### Parameters  
 `lpszFind`  
 The text to be found.  
  
 `bNext`  
 Specifies the direction of the search. If **TRUE**, the search direction is toward the end of the buffer. If **FALSE**, the search direction is toward the beginning of the buffer.  
  
 `bCase`  
 Specifies whether the search is case sensitive. If **TRUE**, the search is case sensitive. If **FALSE**, the search is not case sensitive.  
  
## Return Value  
 Nonzero if the search text is found; otherwise 0.  
  
## Remarks  
 This function searches the text in the buffer for the text specified by `lpszFind`, starting at the current selection, in the direction specified by `bNext`, and with case sensitivity specified by `bCase`. If the text is found, it sets the selection to the found text and returns a nonzero value. If the text is not found, the function returns 0.  
  
 You normally do not need to call the `FindText` function unless you override `OnFindNext`, which calls `FindText`.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CEditView Class](../vs140/CEditView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CEditView::OnFindNext](../vs140/CEditView--OnFindNext.md)   
 [CEditView::OnReplaceAll](../vs140/CEditView--OnReplaceAll.md)   
 [CEditView::OnReplaceSel](../vs140/CEditView--OnReplaceSel.md)   
 [CEditView::OnTextNotFound](../vs140/CEditView--OnTextNotFound.md)