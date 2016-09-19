---
title: "CMDIFrameWndEx::CreateDocumentWindow"
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
ms.assetid: 681f72da-ad49-4d90-aadc-1718e0d4b405
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIFrameWndEx::CreateDocumentWindow
Creates a child document window.  
  
## Syntax  
  
```  
  
      virtual CMDIChildWndEx* CreateDocumentWindow(  
   LPCTSTR lpcszDocName,  
   CObject* pObj  
);  
```  
  
#### Parameters  
 [in] `lpcszDocName`  
 A text string that contains a document identifier. Typically, it is the full path of a document file.  
  
 [in] `pObj`  
 A pointer to a user-defined object. For example, a developer can create an application-specific data structure describing the document and telling how the document should be initialized at startup.  
  
## Return Value  
 A pointer to `CMDIChildWndEx`.  
  
## Remarks  
 The framework calls this method when it loads the list of documents previously saved in the registry.  
  
 Override this method in order to create documents when they are being loaded from the registry.  
  
## Example  
 The following example shows how `CreateDocumentWindow` is used in the [VisualStudioDemo Sample: MFC Visual Studio Application](../vs140/Visual-C---Samples.md).  
  
 In this example, `g_strStartViewName` could be the name of a "virtual document" (for example, "Start Page") that is not actually loaded from a disk file. Therefore we need special processing to handle that case.  
  
 [!CODE [NVC_MFC_VisualStudioDemo#13](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_VisualStudioDemo#13)]  
  
## Requirements  
 **Header:** afxMDIFrameWndEx.h  
  
## See Also  
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMDIFrameWndEx Class](../vs140/CMDIFrameWndEx-Class.md)