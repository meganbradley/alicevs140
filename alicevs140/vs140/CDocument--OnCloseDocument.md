---
title: "CDocument::OnCloseDocument"
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
ms.assetid: fb1e239f-4981-429c-aee4-5403b08074ee
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDocument::OnCloseDocument
Called by the framework when the document is closed, typically as part of the File Close command.  
  
## Syntax  
  
```  
  
virtual void OnCloseDocument( );  
```  
  
## Remarks  
 The default implementation of this function destroys all of the frames used for viewing the document, closes the view, cleans up the document's contents, and then calls the [DeleteContents](../vs140/CDocument--DeleteContents.md) member function to delete the document's data.  
  
 Override this function if you want to perform special cleanup processing when the framework closes a document. For example, if the document represents a record in a database, you may want to override this function to close the database. You should call the base class version of this function from your override.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDocument Class](../vs140/CDocument-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDocument::DeleteContents](../vs140/CDocument--DeleteContents.md)   
 [CDocument::OnNewDocument](../vs140/CDocument--OnNewDocument.md)   
 [CDocument::OnOpenDocument](../vs140/CDocument--OnOpenDocument.md)