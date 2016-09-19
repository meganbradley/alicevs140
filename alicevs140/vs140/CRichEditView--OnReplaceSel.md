---
title: "CRichEditView::OnReplaceSel"
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
ms.assetid: 14298560-cf20-4b1e-aa6f-c0d39034326e
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditView::OnReplaceSel
Called by the framework when processing Replace commands from the Replace dialog box.  
  
## Syntax  
  
```  
  
      virtual void OnReplaceSel(  
   LPCTSTR lpszFind,  
   BOOL bNext,  
   BOOL bCase,  
   BOOL bWord,  
   LPCTSTR lpszReplace   
);  
```  
  
#### Parameters  
 `lpszFind`  
 The text to be replaced.  
  
 `bNext`  
 Indicates the direction of the search: **TRUE** is down; **FALSE**, up.  
  
 `bCase`  
 Indicates if the search is case sensitive.  
  
 `bWord`  
 Indicates if the search must select whole words or not.  
  
 `lpszReplace`  
 The replacement text.  
  
## Remarks  
 Call this function to replace one occurrence of some given text with another string. Override this function to alter search characteristics for this view.  
  
## Requirements  
 **Header:** afxrich.h  
  
## See Also  
 [CRichEditView Class](../vs140/CRichEditView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditView::OnReplaceAll](../vs140/CRichEditView--OnReplaceAll.md)