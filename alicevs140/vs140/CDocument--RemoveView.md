---
title: "CDocument::RemoveView"
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
ms.assetid: 3b4d8ec0-9ce2-4647-aa20-57a2262347a8
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDocument::RemoveView
Call this function to detach a view from a document.  
  
## Syntax  
  
```  
  
      void RemoveView(  
   CView* pView   
);  
```  
  
#### Parameters  
 `pView`  
 Points to the view being removed.  
  
## Remarks  
 This function removes the specified view from the list of views associated with the document; it also sets the view's document pointer to **NULL**. This function is called by the framework when a frame window is closed or a pane of a splitter window is closed.  
  
 Call this function only if you are manually detaching a view. Typically you will let the framework detach documents and views by defining a [CDocTemplate](../vs140/CDocTemplate-Class.md) object to associate a document class, view class, and frame window class.  
  
 See the example at [AddView](../vs140/CDocument--AddView.md) for a sample implementation.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDocument Class](../vs140/CDocument-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDocument::AddView](../vs140/CDocument--AddView.md)   
 [CDocument::GetFirstViewPosition](../vs140/CDocument--GetFirstViewPosition.md)   
 [CDocument::GetNextView](../vs140/CDocument--GetNextView.md)