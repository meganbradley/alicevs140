---
title: "CMDIChildWndEx::GetDocumentName"
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
ms.assetid: 6e2be2f9-08a8-4d52-a477-388e2422a094
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIChildWndEx::GetDocumentName
Returns the name of the document that is displayed in the MDI child window.  
  
## Syntax  
  
```  
virtual LPCTSTR GetDocumentName(  
   CObject** pObj   
);  
```  
  
## Return Value  
 A pointer to a string that contains the name of a document.  
  
## Remarks  
 A document is what the MDI child window displays. Generally, the window displays data that is loaded from or saved to a file. Therefore, the name of the document is the name of the file. The default implementation of `GetDocumentName` returns a string obtained from `CDocument::GetPathName`.  
  
 If the window displays a document that is not loaded from a file, override this method in a derived class and return a unique document identifier.  
  
 `GetDocumentName` is called by the framework when it saves the state of all opened documents. The returned string is written to the registry.  
  
 When the framework is restoring state later, the document name is read from the registry and passed to [CMDIFrameWndEx::CreateDocumentWindow](../vs140/CMDIFrameWndEx--CreateDocumentWindow.md). Override this method in a [CMDIFrameWndEx](../vs140/CMDIFrameWndEx-Class.md)-derived class and create or open a document that has this name and read in the file that has this name. If the document is not based on a file, create the document based on the document identifier itself. You should do the preceding actions only if you intend to save and restore documents.  
  
## Example  
 The following example demonstrates the use of the `GetDocumentName` method. This code snippet comes from the [VisualStudioDemo Sample: MFC Visual Studio Application](../vs140/Visual-C---Samples.md).  
  
 [!CODE [NVC_MFC_VisualStudioDemo#17](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_VisualStudioDemo#17)]  
  
## Requirements  
 **Header:** afxMDIChildWndEx.h  
  
## See Also  
 [CMDIChildWndEx Class](../vs140/CMDIChildWndEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)