---
title: "CRichEditView::OnReplaceAll"
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
ms.assetid: ca6788e7-e425-4149-bd9a-aa856df64834
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditView::OnReplaceAll
Called by the framework when processing Replace All commands from the Replace dialog box.  
  
## Syntax  
  
```  
  
      virtual void OnReplaceAll(  
   LPCTSTR lpszFind,  
   LPCTSTR lpszReplace,  
   BOOL bCase,  
   BOOL bWord   
);  
```  
  
#### Parameters  
 `lpszFind`  
 The text to be replaced.  
  
 `lpszReplace`  
 The replacement text.  
  
 `bCase`  
 Indicates if the search is case sensitive.  
  
 `bWord`  
 Indicates if the search must select whole words or not.  
  
## Remarks  
 Call this function to replace all occurrences of some given text with another string. Override this function to alter search characteristics for this view.  
  
## Example  
 See the example for [CRichEditView::FindText](../vs140/CRichEditView--FindText.md).  
  
## Requirements  
 **Header:** afxrich.h  
  
## See Also  
 [CRichEditView Class](../vs140/CRichEditView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditView::OnReplaceSel](../vs140/CRichEditView--OnReplaceSel.md)   
 [CRichEditView::OnFindNext](../vs140/CRichEditView--OnFindNext.md)