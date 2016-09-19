---
title: "CEditView::OnReplaceSel"
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
ms.assetid: ed425db7-c941-409b-8a21-6b0029f1b72e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CEditView::OnReplaceSel
`CEditView` calls `OnReplaceSel` when the user selects the Replace button in the standard Replace dialog box.  
  
## Syntax  
  
```  
  
      virtual void OnReplaceSel(  
   LPCTSTR lpszFind,  
   BOOL bNext,  
   BOOL bCase,  
   LPCTSTR lpszReplace   
);  
```  
  
#### Parameters  
 `lpszFind`  
 The text to be found.  
  
 `bNext`  
 Specifies the direction of the search. If **TRUE**, the search direction is toward the end of the buffer. If **FALSE**, the search direction is toward the beginning of the buffer.  
  
 `bCase`  
 Specifies whether the search is case sensitive. If **TRUE**, the search is case sensitive. If **FALSE**, the search is not case sensitive.  
  
 `lpszReplace`  
 The text to replace the found text.  
  
## Remarks  
 After replacing the selection, this function searches the text in the buffer for the next occurrence of the text specified by `lpszFind`, in the direction specified by `bNext`, with case sensitivity specified by `bCase`. The search is accomplished through a call to [FindText](../vs140/CEditView--FindText.md). If the text is not found, [OnTextNotFound](../vs140/CEditView--OnTextNotFound.md) is called.  
  
 Override `OnReplaceSel` to change the way a `CEditView`-derived object replaces the selected text.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CEditView Class](../vs140/CEditView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CEditView::OnFindNext](../vs140/CEditView--OnFindNext.md)   
 [CEditView::OnTextNotFound](../vs140/CEditView--OnTextNotFound.md)   
 [CEditView::FindText](../vs140/CEditView--FindText.md)   
 [CEditView::OnReplaceAll](../vs140/CEditView--OnReplaceAll.md)