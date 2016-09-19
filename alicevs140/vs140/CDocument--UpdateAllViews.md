---
title: "CDocument::UpdateAllViews"
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
ms.assetid: 7ee165a5-f48b-4065-b497-63cf8682b152
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDocument::UpdateAllViews
Call this function after the document has been modified.  
  
## Syntax  
  
```  
  
      void UpdateAllViews(  
   CView* pSender,  
   LPARAM lHint = 0L,  
   CObject* pHint = NULL   
);  
```  
  
#### Parameters  
 `pSender`  
 Points to the view that modified the document, or **NULL** if all views are to be updated.  
  
 `lHint`  
 Contains information about the modification.  
  
 `pHint`  
 Points to an object storing information about the modification.  
  
## Remarks  
 You should call this function after you call the [SetModifiedFlag](../vs140/CDocument--SetModifiedFlag.md) member function. This function informs each view attached to the document, except for the view specified by `pSender`, that the document has been modified. You typically call this function from your view class after the user has changed the document through a view.  
  
 This function calls the [CView::OnUpdate](../vs140/CView--OnUpdate.md) member function for each of the document's views except the sending view, passing `pHint` and `lHint`. Use these parameters to pass information to the views about the modifications made to the document. You can encode information using `lHint` and/or you can define a [CObject](../vs140/CObject-Class.md)-derived class to store information about the modifications and pass an object of that class using `pHint`. Override the `CView::OnUpdate` member function in your [CView](../vs140/CView-Class.md)-derived class to optimize the updating of the view's display based on the information passed.  
  
## Example  
 [!CODE [NVC_MFCDocView#64](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#64)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDocument Class](../vs140/CDocument-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDocument::SetModifiedFlag](../vs140/CDocument--SetModifiedFlag.md)   
 [CDocument::GetFirstViewPosition](../vs140/CDocument--GetFirstViewPosition.md)   
 [CDocument::GetNextView](../vs140/CDocument--GetNextView.md)   
 [CView::OnUpdate](../vs140/CView--OnUpdate.md)