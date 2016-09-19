---
title: "CDocument::DeleteContents"
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
ms.assetid: 14f57f45-0c5f-4d83-b75f-64769e01814d
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDocument::DeleteContents
Called by the framework to delete the document's data without destroying the **CDocument** object itself.  
  
## Syntax  
  
```  
  
virtual void DeleteContents( );  
```  
  
## Remarks  
 It is called just before the document is to be destroyed. It is also called to ensure that a document is empty before it is reused. This is particularly important for an SDI application, which uses only one document; the document is reused whenever the user creates or opens another document. Call this function to implement an "Edit Clear All" or similar command that deletes all of the document's data. The default implementation of this function does nothing. Override this function to delete the data in your document.  
  
## Example  
 [!CODE [NVC_MFCDocView#57](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#57)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDocument Class](../vs140/CDocument-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDocument::OnCloseDocument](../vs140/CDocument--OnCloseDocument.md)   
 [CDocument::OnNewDocument](../vs140/CDocument--OnNewDocument.md)   
 [CDocument::OnOpenDocument](../vs140/CDocument--OnOpenDocument.md)