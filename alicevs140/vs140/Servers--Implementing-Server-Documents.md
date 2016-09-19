---
title: "Servers: Implementing Server Documents"
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
ms.assetid: cca1451a-ad09-47ed-b56e-bccd78fc86d1
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Servers: Implementing Server Documents
This article explains the steps you must take to successfully implement a server document if you did not specify the OLE Server option in the application wizard.  
  
#### To define a server document class  
  
1.  Derive your document class from `COleServerDoc` instead of **CDocument**.  
  
2.  Create a server item class derived from `COleServerItem`.  
  
3.  Implement the `OnGetEmbeddedItem` member function of your server document class.  
  
     `OnGetEmbeddedItem` is called when the user of a container application creates or edits an embedded item. It should return an item representing the entire document. This should be an object of your `COleServerItem`-derived class.  
  
4.  Override the `Serialize` member function to serialize the contents of the document. You do not need to serialize the list of server items unless you are using them to represent the native data in your document. For more information, see *Implementing Server Items* in the article [Servers: Server Items](../vs140/Servers--Server-Items.md).  
  
 When a server document is created, the framework automatically registers the document with the OLE system DLLs. This allows the DLLs to identify the server documents.  
  
 For more information, see [COleServerItem](../vs140/COleServerItem-Class.md) and [COleServerDoc](../vs140/COleServerDoc-Class.md) in the *Class Library Reference*.  
  
## See Also  
 [Servers](../vs140/Servers.md)   
 [Servers: Server Items](../vs140/Servers--Server-Items.md)   
 [Servers: Implementing a Server](../vs140/Servers--Implementing-a-Server.md)   
 [Servers: Implementing In-Place Frame Windows](../vs140/Servers--Implementing-In-Place-Frame-Windows.md)