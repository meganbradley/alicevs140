---
title: "CRichEditView::OnFindNext"
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
ms.assetid: ccff9731-4d19-4369-b4a5-93d7e8c24ce1
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditView::OnFindNext
Called by the framework when processing commands from the Find/Replace dialog box.  
  
## Syntax  
  
```  
  
      virtual void OnFindNext(  
   LPCTSTR lpszFind,  
   BOOL bNext,  
   BOOL bCase,  
   BOOL bWord   
);  
```  
  
#### Parameters  
 `lpszFind`  
 The string to find.  
  
 `bNext`  
 The direction to search: **TRUE** indicates down; **FALSE**, up.  
  
 `bCase`  
 Indicates whether the search is to be case sensitive.  
  
 `bWord`  
 Indicates whether the search is to match whole words only or not.  
  
## Remarks  
 Call this function to find text within the `CRichEditView`. Override this function to alter search characteristics for your derived view class.  
  
## Requirements  
 **Header:** afxrich.h  
  
## See Also  
 [CRichEditView Class](../vs140/CRichEditView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditView::FindText](../vs140/CRichEditView--FindText.md)   
 [CRichEditView::FindTextSimple](../vs140/CRichEditView--FindTextSimple.md)