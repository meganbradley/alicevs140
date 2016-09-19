---
title: "CDocObjectServer::CDocObjectServer"
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
ms.assetid: 51510e3e-4b4f-495a-a0f9-28fae3252874
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDocObjectServer::CDocObjectServer
Constructs and initializes a `CDocObjectServer` object.  
  
## Syntax  
  
```  
  
      explicit CDocObjectServer(   
   COleServerDoc* pOwner,   
   LPOLEDOCUMENTSITE pDocSite = NULL    
);  
```  
  
#### Parameters  
 *pOwner*  
 A pointer to the client site document that is the client for the DocObject server.  
  
 `pDocSite`  
 A pointer to the `IOleDocumentSite` interface implemented by the container.  
  
## Remarks  
 When a DocObject is active, the client site OLE interface (`IOleDocumentSite`) is what allows the DocObject server to communicate with its client (the container). When a DocObject server is activated, it first checks that the container implements the `IOleDocumentSite` interface. If so, [COleServerDoc::GetDocObjectServer](../vs140/COleServerDoc--GetDocObjectServer.md) is called to see if the container supports DocObjects. By default, `GetDocObjectServer` returns **NULL**. You must override `COleServerDoc::GetDocObjectServer` to construct a new `CDocObjectServer` object or a derived object of your own, with pointers to the `COleServerDoc` container and its `IOleDocumentSite` interface as arguments to the constructor.  
  
## Requirements  
 **Header:** afxdocob.h  
  
## See Also  
 [CDocObjectServer Class](../vs140/CDocObjectServer-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDocObjectServerItem Class](../vs140/CDocObjectServerItem-Class.md)   
 [COleServerDoc::GetDocObjectServer](../vs140/COleServerDoc--GetDocObjectServer.md)