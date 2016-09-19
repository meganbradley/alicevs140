---
title: "CDocument::AddView"
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
ms.assetid: 7bcd7c7a-39b8-4359-bb7c-2c1b49683269
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDocument::AddView
Call this function to attach a view to the document.  
  
## Syntax  
  
```  
  
      void AddView(  
   CView* pView   
);  
```  
  
#### Parameters  
 `pView`  
 Points to the view being added.  
  
## Remarks  
 This function adds the specified view to the list of views associated with the document; the function also sets the view's document pointer to this document. The framework calls this function when attaching a newly created view object to a document; this occurs in response to a File New, File Open, or New Window command or when a splitter window is split.  
  
 Call this function only if you are manually creating and attaching a view. Typically you will let the framework connect documents and views by defining a [CDocTemplate](../vs140/CDocTemplate-Class.md) object to associate a document class, view class, and frame window class.  
  
## Example  
 [!CODE [NVC_MFCDocViewSDI#12](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocViewSDI#12)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDocument Class](../vs140/CDocument-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDocTemplate Class](../vs140/CDocTemplate-Class.md)   
 [CDocument::GetFirstViewPosition](../vs140/CDocument--GetFirstViewPosition.md)   
 [CDocument::GetNextView](../vs140/CDocument--GetNextView.md)   
 [CDocument::RemoveView](../vs140/CDocument--RemoveView.md)   
 [CView::GetDocument](../vs140/CView--GetDocument.md)