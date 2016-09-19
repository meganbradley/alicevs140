---
title: "COleServerDoc::GetDocObjectServer"
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
ms.assetid: 388ad289-91f3-4651-a7b2-5015a0ce6e8f
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleServerDoc::GetDocObjectServer
Override this function to create a new `CDocObjectServer` item and return a pointer to it.  
  
## Syntax  
  
```  
  
      virtual CDocObjectServer* GetDocObjectServer(   
   LPOLEDOCUMENTSITE pDocSite    
);  
```  
  
#### Parameters  
 `pDocSite`  
 Pointer to the `IOleDocumentSite` interface that will connect this document to the server.  
  
## Return Value  
 A pointer to a `CDocObjectServer`; **NULL** if the operation failed.  
  
## Remarks  
 When a DocObject server is activated, the return of a non-**NULL** pointer shows that the client can support DocObjects. The default implementation returns **NULL**.  
  
 A typical implementation for a document that supports DocObjects will simply allocate a new `CDocObjectServer` object and return it to the caller. For example:  
  
 [!CODE [NVC_MFCOleServer#3](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCOleServer#3)]  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleServerDoc Class](../vs140/COleServerDoc-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDocObjectServer::CDocObjectServer](../vs140/CDocObjectServer--CDocObjectServer.md)