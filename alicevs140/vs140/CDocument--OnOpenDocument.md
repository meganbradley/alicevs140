---
title: "CDocument::OnOpenDocument"
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
ms.assetid: 357b6f7b-091b-426c-b1a5-9affadf1e3d3
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDocument::OnOpenDocument
Called by the framework as part of the File Open command.  
  
## Syntax  
  
```  
  
      virtual BOOL OnOpenDocument(  
   LPCTSTR lpszPathName   
);  
```  
  
#### Parameters  
 `lpszPathName`  
 Points to the path of the document to be opened.  
  
## Return Value  
 Nonzero if the document was successfully loaded; otherwise 0.  
  
## Remarks  
 The default implementation of this function opens the specified file, calls the [DeleteContents](../vs140/CDocument--DeleteContents.md) member function to ensure that the document is empty, calls [CObject::Serialize](../vs140/CObject--Serialize.md) to read the file's contents, and then marks the document as clean. Override this function if you want to use something other than the archive mechanism or the file mechanism. For example, you might write an application where documents represent records in a database rather than separate files.  
  
 If the user chooses the File Open command in an SDI application, the framework uses this function to reinitialize the existing **CDocument** object, rather than creating a new one. If the user chooses File Open in an MDI application, the framework constructs a new **CDocument** object each time and then calls this function to initialize it. You must place your initialization code in this function instead of in the constructor for the File Open command to be effective in SDI applications.  
  
## Example  
 The following examples illustrate alternative methods of initializing a document object.  
  
 [!CODE [NVC_MFCDocView#60](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#60)]  
  
 [!CODE [NVC_MFCDocView#61](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#61)]  
  
 [!CODE [NVC_MFCDocView#62](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#62)]  
  
 [!CODE [NVC_MFCDocView#63](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#63)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDocument Class](../vs140/CDocument-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDocument::DeleteContents](../vs140/CDocument--DeleteContents.md)   
 [CDocument::OnCloseDocument](../vs140/CDocument--OnCloseDocument.md)   
 [CDocument::OnNewDocument](../vs140/CDocument--OnNewDocument.md)   
 [CDocument::OnSaveDocument](../vs140/CDocument--OnSaveDocument.md)   
 [CDocument::ReportSaveLoadException](../vs140/CDocument--ReportSaveLoadException.md)   
 [CObject::Serialize](../vs140/CObject--Serialize.md)