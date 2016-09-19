---
title: "CRichEditView::OnInitialUpdate"
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
ms.assetid: 25944e9f-f924-46ab-ac54-a25f34e06f14
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditView::OnInitialUpdate
Called by the framework after the view is first attached to the document, but before the view is initially displayed.  
  
## Syntax  
  
```  
  
virtual void OnInitialUpdate( );  
  
```  
  
## Remarks  
 The default implementation of this function calls the [CView::OnUpdate](../vs140/CView--OnUpdate.md) member function with no hint information (that is, using the default values of 0 for the `lHint` parameter and **NULL** for the `pHint` parameter). Override this function to perform any one-time initialization that requires information about the document. For example, if your application has fixed-sized documents, you can use this function to initialize a view's scrolling limits based on the document size. If your application supports variable-sized documents, use `OnUpdate` to update the scrolling limits every time the document changes.  
  
## Example  
 See the example for [CRichEditView::m_nWordWrap](../vs140/CRichEditView--m_nWordWrap.md).  
  
## Requirements  
 **Header:** afxrich.h  
  
## See Also  
 [CRichEditView Class](../vs140/CRichEditView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CView::OnUpdate](../vs140/CView--OnUpdate.md)