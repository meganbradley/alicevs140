---
title: "Containers: Client Items"
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
ms.assetid: 231528b5-0744-4f83-8897-083bf55ed087
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Containers: Client Items
This article explains what client items are and from what classes your application should derive its client items.  
  
 Client items are data items belonging to another application that are either contained in or referenced by an OLE container application's document. Client items whose data is contained within the document are embedded; those whose data is stored in another location referenced by the container document are linked.  
  
 The document class in an OLE application is derived from the class [COleDocument](../vs140/COleDocument-Class.md) rather than from **CDocument**. The `COleDocument` class inherits from **CDocument** all the functionality necessary for using the document/view architecture on which MFC applications are based. `COleDocument` also defines an interface that treats a document as a collection of `CDocItem` objects. Several `COleDocument` member functions are provided for adding, retrieving, and deleting elements of that collection.  
  
 Every container application should derive at least one class from `COleClientItem`. Objects of this class represent items, embedded or linked, in the OLE document. These objects exist for the life of the document containing them, unless they are deleted from the document.  
  
 `CDocItem` is the base class for `COleClientItem` and `COleServerItem`. Objects of classes derived from these two act as intermediaries between the OLE item and the client and server applications, respectively. Each time a new OLE item is added to the document, the MFC framework adds a new object of your client application's `COleClientItem`-derived class to the document's collection of `CDocItem` objects.  
  
## See Also  
 [Containers](../vs140/Containers.md)   
 [Containers: Compound Files](../vs140/Containers--Compound-Files.md)   
 [Containers: User-Interface Issues](../vs140/Containers--User-Interface-Issues.md)   
 [Containers: Advanced Features](../vs140/Containers--Advanced-Features.md)   
 [COleClientItem Class](../vs140/COleClientItem-Class.md)   
 [COleServerItem Class](../vs140/COleServerItem-Class.md)