---
title: "CDocument::OnNewDocument"
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
ms.assetid: 8a31fa20-81b6-450d-81d4-064d39111909
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDocument::OnNewDocument
Called by the framework as part of the File New command.  
  
## Syntax  
  
```  
  
virtual BOOL OnNewDocument( );  
```  
  
## Return Value  
 Nonzero if the document was successfully initialized; otherwise 0.  
  
## Remarks  
 The default implementation of this function calls the [DeleteContents](../vs140/CDocument--DeleteContents.md) member function to ensure that the document is empty and then marks the new document as clean. Override this function to initialize the data structure for a new document. You should call the base class version of this function from your override.  
  
 If the user chooses the File New command in an SDI application, the framework uses this function to reinitialize the existing document, rather than creating a new one. If the user chooses File New in a multiple document interface (MDI) application, the framework creates a new document each time and then calls this function to initialize it. You must place your initialization code in this function instead of in the constructor for the File New command to be effective in SDI applications.  
  
 Note that there are cases where `OnNewDocument` is called twice. This occurs when the document is embedded as an ActiveX Document Server. The function is first called by the `CreateInstance` method (exposed by the `COleObjectFactory`-derived class) and a second time by the `InitNew` method (exposed by the `COleServerDoc`-derived class).  
  
## Example  
 The following examples illustrate alternative methods of initializing a document object.  
  
 [!CODE [NVC_MFCDocView#60](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#60)]  
  
 [!CODE [NVC_MFCDocView#61](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#61)]  
  
 [!CODE [NVC_MFCDocView#62](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#62)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDocument Class](../vs140/CDocument-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDocument::CDocument](../vs140/CDocument--CDocument.md)   
 [CDocument::DeleteContents](../vs140/CDocument--DeleteContents.md)   
 [CDocument::OnCloseDocument](../vs140/CDocument--OnCloseDocument.md)   
 [CDocument::OnOpenDocument](../vs140/CDocument--OnOpenDocument.md)   
 [CDocument::OnSaveDocument](../vs140/CDocument--OnSaveDocument.md)