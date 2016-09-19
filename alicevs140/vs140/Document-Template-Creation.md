---
title: "Document Template Creation"
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
ms.topic: article
ms.assetid: c87f1821-7cbf-442e-9690-f126ae7fb783
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Document Template Creation
When creating a new document in response to a `New` or **Open** command from the **File** menu, the document template also creates a new frame window through which to view the document.  
  
 The document-template constructor specifies what types of documents, windows, and views the template will be able to create. This is determined by the arguments you pass to the document-template constructor. The following code illustrates creation of a [CMultiDocTemplate](../vs140/CMultiDocTemplate-Class.md) for a sample application:  
  
 [!CODE [NVC_MFCDocView#7](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#7)]  
  
 The pointer to a new `CMultiDocTemplate` object is used as an argument to [AddDocTemplate](../vs140/CWinApp--AddDocTemplate.md). Arguments to the `CMultiDocTemplate` constructor include the resource ID associated with the document type's menus and accelerators, and three uses of the [RUNTIME_CLASS](../vs140/RUNTIME_CLASS.md) macro. `RUNTIME_CLASS` returns the [CRuntimeClass](../vs140/CRuntimeClass-Structure.md) object for the C++ class named as its argument. The three `CRuntimeClass` objects passed to the document-template constructor supply the information needed to create new objects of the specified classes during the document creation process. The example shows creation of a document template that creates `CScribDoc` objects with `CScribView` objects attached. The views are framed by standard MDI child frame windows.  
  
## See Also  
 [Document Templates and the Document/View Creation Process](../vs140/Document-Templates-and-the-Document-View-Creation-Process.md)   
 [Document/View Creation](../vs140/Document-View-Creation.md)   
 [Relationships Among MFC Objects](../vs140/Relationships-Among-MFC-Objects.md)   
 [Creating New Documents, Windows, and Views](../vs140/Creating-New-Documents--Windows--and-Views.md)