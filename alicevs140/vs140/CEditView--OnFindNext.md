---
title: "CEditView::OnFindNext"
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
ms.assetid: 60e5843a-d18b-4be8-9662-eb4d8fa2606f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CEditView::OnFindNext
Searches the text in the buffer for the text specified by `lpszFind`, in the direction specified by `bNext`, with case sensitivity specified by `bCase`.  
  
## Syntax  
  
```  
  
      virtual void OnFindNext(   
   LPCTSTR lpszFind,   
   BOOL bNext,   
   BOOL bCase    
);  
```  
  
#### Parameters  
 `lpszFind`  
 The text to be found.  
  
 `bNext`  
 Specifies the direction of the search. If **TRUE**, the search direction is toward the end of the buffer. If **FALSE**, the search direction is toward the beginning of the buffer.  
  
 `bCase`  
 Specifies whether the search is case sensitive. If **TRUE**, the search is case sensitive. If **FALSE**, the search is not case sensitive.  
  
## Remarks  
 The search starts at the beginning of the current selection and is accomplished through a call to [FindText](../vs140/CEditView--FindText.md). In the default implementation, `OnFindNext` calls [OnTextNotFound](../vs140/CEditView--OnTextNotFound.md) if the text is not found.  
  
 Override `OnFindNext` to change the way a `CEditView`-derived object searches text. `CEditView` calls `OnFindNext` when the user chooses the Find Next button in the standard Find dialog box.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CEditView Class](../vs140/CEditView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CEditView::OnTextNotFound](../vs140/CEditView--OnTextNotFound.md)   
 [CEditView::FindText](../vs140/CEditView--FindText.md)   
 [CEditView::OnReplaceAll](../vs140/CEditView--OnReplaceAll.md)   
 [CEditView::OnReplaceSel](../vs140/CEditView--OnReplaceSel.md)