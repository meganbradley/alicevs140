---
title: "CDocument::OnChangedViewList"
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
ms.assetid: 75c402df-1b5d-4e43-8479-bac9385864c4
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDocument::OnChangedViewList
Called by the framework after a view is added to or removed from the document.  
  
## Syntax  
  
```  
  
virtual void OnChangedViewList( );  
```  
  
## Remarks  
 The default implementation of this function checks whether the last view is being removed and, if so, deletes the document. Override this function if you want to perform special processing when the framework adds or removes a view. For example, if you want a document to remain open even when there are no views attached to it, override this function.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDocument Class](../vs140/CDocument-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDocument::AddView](../vs140/CDocument--AddView.md)   
 [CDocument::RemoveView](../vs140/CDocument--RemoveView.md)