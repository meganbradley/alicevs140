---
title: "CEditView::OnReplaceAll"
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
ms.assetid: 9da3567b-4a1a-4497-8507-95a97379a718
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CEditView::OnReplaceAll
`CEditView` calls `OnReplaceAll` when the user selects the Replace All button in the standard Replace dialog box.  
  
## Syntax  
  
```  
  
      virtual void OnReplaceAll(  
   LPCTSTR lpszFind,  
   LPCTSTR lpszReplace,  
   BOOL bCase   
);  
```  
  
#### Parameters  
 `lpszFind`  
 The text to be found.  
  
 `lpszReplace`  
 The text to replace the search text.  
  
 `bCase`  
 Specifies whether search is case sensitive. If **TRUE**, the search is case sensitive. If **FALSE**, the search is not case sensitive.  
  
## Remarks  
 `OnReplaceAll` searches the text in the buffer for the text specified by `lpszFind`, with case sensitivity specified by `bCase`. The search starts at the beginning of the current selection. Each time the search text is found, this function replaces that occurrence of the text with the text specified by `lpszReplace`. The search is accomplished through a call to [FindText](../vs140/CEditView--FindText.md). In the default implementation, [OnTextNotFound](../vs140/CEditView--OnTextNotFound.md) is called if the text is not found.  
  
 If the current selection does not match `lpszFind`, the selection is updated to the first occurrence of the text specified by `lpszFind` and a replace is not performed. This allows the user to confirm that this is what they want to do when the selection does not match the text to be replaced.  
  
 Override `OnReplaceAll` to change the way a `CEditView`-derived object replaces text.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CEditView Class](../vs140/CEditView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CEditView::OnFindNext](../vs140/CEditView--OnFindNext.md)   
 [CEditView::OnTextNotFound](../vs140/CEditView--OnTextNotFound.md)   
 [CEditView::FindText](../vs140/CEditView--FindText.md)   
 [CEditView::OnReplaceSel](../vs140/CEditView--OnReplaceSel.md)