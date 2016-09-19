---
title: "Using Documents"
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
ms.assetid: f390d6d8-d0e1-4497-9b6a-435f7ce0776c
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Using Documents
Working together, documents and views:  
  
-   Contain, manage, and display your application-specific [data](../vs140/Managing-Data-with-Document-Data-Variables.md).  
  
-   Provide an interface consisting of [document data variables](../vs140/Managing-Data-with-Document-Data-Variables.md) for manipulating the data.  
  
-   Participate in [writing and reading files](../vs140/Serializing-Data-to-and-from-Files.md).  
  
-   Participate in [printing](../vs140/Role-of-the-View-in-Printing.md).  
  
-   [Handle](../vs140/Handling-Commands-in-the-Document.md) most of your application's commands and messages.  
  
 The document is particularly involved in managing data. Store your data, normally, in document class member variables. The view uses these variables to access the data for display and update. The document's default serialization mechanism manages reading and writing the data to and from files. Documents can also handle commands (but not Windows messages other than **WM_COMMAND**).  
  
## What do you want to know more about?  
  
-   [Deriving a document class from CDocument](../vs140/Deriving-a-Document-Class-from-CDocument.md)  
  
-   [Managing data with document data variables](../vs140/Managing-Data-with-Document-Data-Variables.md)  
  
-   [Serializing data to and from files](../vs140/Serializing-Data-to-and-from-Files.md)  
  
-   [Bypassing the serialization mechanism](../vs140/Bypassing-the-Serialization-Mechanism.md)  
  
-   [Handling commands in the document](../vs140/Handling-Commands-in-the-Document.md)  
  
-   [The OnNewDocument member function](../vs140/CDocument--OnNewDocument.md)  
  
-   [The DeleteContents member function](../vs140/CDocument--DeleteContents.md)  
  
## See Also  
 [Document/View Architecture](../vs140/Document-View-Architecture.md)