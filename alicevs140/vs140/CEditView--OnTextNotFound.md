---
title: "CEditView::OnTextNotFound"
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
ms.assetid: 72f1fa75-965f-4823-9871-785295cbabb8
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CEditView::OnTextNotFound
Override this function to change the default implementation, which calls the Windows function **MessageBeep**.  
  
## Syntax  
  
```  
  
      virtual void OnTextNotFound(  
   LPCTSTR lpszFind   
);  
```  
  
#### Parameters  
 `lpszFind`  
 The text to be found.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CEditView Class](../vs140/CEditView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CEditView::FindText](../vs140/CEditView--FindText.md)   
 [CEditView::OnFindNext](../vs140/CEditView--OnFindNext.md)   
 [CEditView::OnReplaceAll](../vs140/CEditView--OnReplaceAll.md)   
 [CEditView::OnReplaceSel](../vs140/CEditView--OnReplaceSel.md)