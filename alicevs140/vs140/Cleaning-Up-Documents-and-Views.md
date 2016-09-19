---
title: "Cleaning Up Documents and Views"
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
ms.assetid: 0c454db2-3644-434d-9e53-8108a7aedfe1
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Cleaning Up Documents and Views
When a document is closing, the framework first calls its [DeleteContents](../vs140/CDocument--DeleteContents.md) member function. If you allocated any memory on the heap during the course of the document's operation, `DeleteContents` is the best place to deallocate it.  
  
> [!NOTE]
>  You should not deallocate document data in the document's destructor. In the case of an SDI application, the document object might be reused.  
  
 You can override a view's destructor to deallocate any memory you allocated on the heap.  
  
## See Also  
 [Initializing and Cleaning Up Documents and Views](../vs140/Initializing-and-Cleaning-Up-Documents-and-Views.md)