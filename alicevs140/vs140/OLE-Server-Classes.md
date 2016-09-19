---
title: "OLE Server Classes"
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
ms.assetid: 8e9b67a2-c0ff-479c-a8d6-19b36c5e6fc6
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# OLE Server Classes
These classes are used by server applications. Server documents are derived from `COleServerDoc` rather than from **CDocument**. Note that because `COleServerDoc` is derived from `COleLinkingDoc`, server documents can also be containers that support linking.  
  
 The `COleServerItem` class represents a document or portion of a document that can be embedded in another document or linked to.  
  
 `COleIPFrameWnd` and `COleResizeBar` support in-place editing while the object is in a container, and `COleTemplateServer` supports creation of document/view pairs so OLE objects from other applications can be edited.  
  
 [COleServerDoc](../vs140/COleServerDoc-Class.md)  
 Used as the base class for server-application document classes. `COleServerDoc` objects provide the bulk of server support through interactions with `COleServerItem` objects. Visual editing capability is provided using the class library's document/view architecture.  
  
 [CDocItem](../vs140/CDocItem-Class.md)  
 Abstract base class of `COleClientItem` and `COleServerItem`. Objects of classes derived from `CDocItem` represent parts of documents.  
  
 [COleServerItem](../vs140/COleServerItem-Class.md)  
 Used to represent the OLE interface to `COleServerDoc` items. There is usually one `COleServerDoc` object, which represents the embedded part of a document. In servers that support links to parts of documents, there can be many `COleServerItem` objects, each of which represents a link to a portion of the document.  
  
 [COleIPFrameWnd](../vs140/COleIPFrameWnd-Class.md)  
 Provides the frame window for a view when a server document is being edited in place.  
  
 [COleResizeBar](../vs140/COleResizeBar-Class.md)  
 Provides the standard user interface for in-place resizing. Objects of this class are always used in conjunction with `COleIPFrameWnd` objects.  
  
 [COleTemplateServer](../vs140/COleTemplateServer-Class.md)  
 Used to create documents using the framework's document/view architecture. A `COleTemplateServer` object delegates most of its work to an associated `CDocTemplate` object.  
  
 [COleException](../vs140/COleException-Class.md)  
 An exception resulting from a failure in OLE processing. This class is used by both containers and servers.  
  
## See Also  
 [Class Overview](../vs140/Class-Library-Overview.md)