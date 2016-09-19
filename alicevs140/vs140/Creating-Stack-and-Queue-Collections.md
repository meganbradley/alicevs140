---
title: "Creating Stack and Queue Collections"
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
ms.assetid: 3c7bc198-35f0-4fc3-aaed-6005a0f22638
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Creating Stack and Queue Collections
This article explains how to create other data structures, such as [stacks](#_core_stacks) and [queues](#_core_queues), from MFC list classes. The examples use classes derived from `CList`, but you can use `CList` directly unless you need to add functionality.  
  
##  <a name="_core_stacks"></a> Stacks  
 Because the standard list collection has both a head and a tail, it is easy to create a derived list collection that mimics the behavior of a last-in-first-out stack. A stack is like a stack of trays in a cafeteria. As trays are added to the stack, they go on top of the stack. The last tray added is the first to be removed. The list collection member functions `AddHead` and `RemoveHead` can be used to add and remove elements specifically from the head of the list; thus, the most recently added element is the first to be removed.  
  
#### To create a stack collection  
  
1.  Derive a new list class from one of the existing MFC list classes and add more member functions to support the functionality of stack operations.  
  
     The following example shows how to add member functions to push elements on to the stack, peek at the top element of the stack, and pop the top element from the stack:  
  
     [!CODE [NVC_MFCCollections#20](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#20)]  
  
 Note that this approach exposes the underlying `CObList` class. The user can call any `CObList` member function, whether it makes sense for a stack or not.  
  
##  <a name="_core_queues"></a> Queues  
 Because the standard list collection has both a head and a tail, it is also easy to create a derived list collection that mimics the behavior of a first-in-first-out queue. A queue is like a line of people in a cafeteria. The first person in line is the first to be served. As more people come, they go to the end of the line to wait their turn. The list collection member functions `AddTail` and `RemoveHead` can be used to add and remove elements specifically from the head or tail of the list; thus, the most recently added element is always the last to be removed.  
  
#### To create a queue collection  
  
1.  Derive a new list class from one of the predefined list classes provided with the Microsoft Foundation Class Library and add more member functions to support the semantics of queue operations.  
  
     The following example shows how you can append member functions to add an element to the end of the queue and get the element from the front of the queue.  
  
     [!CODE [NVC_MFCCollections#21](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#21)]  
  
## See Also  
 [Collections](../vs140/Collections.md)