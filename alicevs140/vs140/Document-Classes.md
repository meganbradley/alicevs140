---
title: "Document Classes"
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
ms.assetid: 4bf19b02-0a4f-4319-b68e-cddcba2705cb
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Document Classes
Document class objects, created by document-template objects, manage the application's data. You will derive a class for your documents from one of these classes.  
  
 Document class objects interact with view objects. View objects represent the client area of a window, display a document's data, and allow users to interact with it. Documents and views are created by a document-template object.  
  
 [CDocument](../vs140/CDocument-Class.md)  
 The base class for application-specific documents. Derive your document class or classes from **CDocument**.  
  
 [COleDocument](../vs140/COleDocument-Class.md)  
 Used for compound document implementation, as well as basic container support. Serves as a container for classes derived from [CDocItem](../vs140/CDocItem-Class.md). This class can be used as the base class for container documents and is the base class for `COleServerDoc`.  
  
 [COleLinkingDoc](../vs140/COleLinkingDoc-Class.md)  
 A class derived from `COleDocument` that provides the infrastructure for linking. You should derive the document classes for your container applications from this class instead of from `COleDocument` if you want them to support links to embedded objects.  
  
 [CRichEditDoc](../vs140/CRichEditDoc-Class.md)  
 Maintains the list of OLE client items that are in the rich edit control. Used with [CRichEditView](../vs140/CRichEditView-Class.md) and [CRichEditCntrItem](../vs140/CRichEditCntrItem-Class.md).  
  
 [COleServerDoc](../vs140/COleServerDoc-Class.md)  
 Used as the base class for server-application document classes. `COleServerDoc` objects provide the bulk of server support through interactions with [COleServerItem](../vs140/COleServerItem-Class.md) objects. Visual editing capability is provided using the class library's document/view architecture.  
  
 [CHtmlEditDoc](../vs140/CHtmlEditDoc-Class.md)  
 Provides, with [CHtmlEditView](../vs140/CHtmlEditView-Class.md), the functionality of the WebBrowser HTML editing platform within the context of the MFC document-view architecture.  
  
## Related Classes  
 Document class objects can be persistent — in other words, they can write their state to a storage medium and read it back. MFC provides the `CArchive` class to facilitate transferring the document's data to a storage medium.  
  
 [CArchive](../vs140/CArchive-Class.md)  
 Cooperates with a [CFile](../vs140/CFile-Class.md) object to implement persistent storage for objects through serialization (see [CObject::Serialize](../vs140/CObject--Serialize.md)).  
  
 Documents can also contain OLE objects. `CDocItem` is the base class of the server and client items.  
  
 [CDocItem](../vs140/CDocItem-Class.md)  
 Abstract base class of [COleClientItem](../vs140/COleClientItem-Class.md) and [COleServerItem](../vs140/COleServerItem-Class.md). Objects of classes derived from `CDocItem` represent parts of documents.  
  
## See Also  
 [Class Overview](../vs140/Class-Library-Overview.md)