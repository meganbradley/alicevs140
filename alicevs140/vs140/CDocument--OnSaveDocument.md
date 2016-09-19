---
title: "CDocument::OnSaveDocument"
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
ms.assetid: f697323b-0f9a-4dd0-8296-fc899db96ab6
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDocument::OnSaveDocument
Called by the framework as part of the File Save or File Save As command.  
  
## Syntax  
  
```  
  
      virtual BOOL OnSaveDocument(  
   LPCTSTR lpszPathName   
);  
```  
  
#### Parameters  
 `lpszPathName`  
 Points to the fully qualified path to which the file should be saved.  
  
## Return Value  
 Nonzero if the document was successfully saved; otherwise 0.  
  
## Remarks  
 The default implementation of this function opens the specified file, calls [CObject::Serialize](../vs140/CObject--Serialize.md) to write the document's data to the file, and then marks the document as clean. Override this function if you want to perform special processing when the framework saves a document. For example, you might write an application where documents represent records in a database rather than separate files.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDocument Class](../vs140/CDocument-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDocument::OnCloseDocument](../vs140/CDocument--OnCloseDocument.md)   
 [CDocument::OnNewDocument](../vs140/CDocument--OnNewDocument.md)   
 [CDocument::OnOpenDocument](../vs140/CDocument--OnOpenDocument.md)   
 [CDocument::ReportSaveLoadException](../vs140/CDocument--ReportSaveLoadException.md)   
 [CObject::Serialize](../vs140/CObject--Serialize.md)