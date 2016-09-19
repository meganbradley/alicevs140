---
title: "Array, List, and Map Classes"
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
ms.assetid: 81a13a7f-0c2c-4efd-b6bb-b4e624a0743d
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Array, List, and Map Classes
For handling aggregates of data, the class library provides a group of collection classes — arrays, lists, and maps — that can hold a variety of object and predefined types. The collections are dynamically sized. These classes can be used in any program, whether written for Windows or not. However, they are most useful for implementing the data structures that define your document classes in the application framework. You can readily derive specialized collection classes from these, or you can create them based on the template classes. For more information about these approaches, see the article [Collections](../vs140/Collections.md). For a list of the template collection classes, see the article [Template Classes for Arrays, Lists, and Maps](../vs140/Template-Classes-for-Arrays--Lists--and-Maps.md).  
  
 Arrays are one-dimensional data structures that are stored contiguously in memory. They support very fast random access since the memory address of any given element can be calculated by multiplying the index of the element by the size of an element and adding the result to the base address of the array. But arrays are very expensive if you have to insert elements into the array, since the entire array past the element inserted has to be moved to make room for the element to be inserted. Arrays can grow and shrink as necessary.  
  
 Lists are similar to arrays but are stored very differently. Each element in a list also includes a pointer to the previous and next elements, making it a doubly linked list. It is very fast to add or delete items because doing so only involves changing a few pointers. However, searching a list can be expensive since all searches need to start at one of the list's ends.  
  
 Maps relate a key value to a data value. For instance, the key of a map could be a string and the data a pointer into a list. You would ask the map to give you the pointer associated with a particular string. Map lookups are fast because maps use hash tables for key lookups. Adding and deleting items is also fast. Maps are often used with other data structures as auxiliary indices. MFC uses a special kind of map called a [message map](../vs140/Mapping-Messages.md) to map Windows messages to a pointer to the handler function for that message.  
  
## See Also  
 [Class Overview](../vs140/Class-Library-Overview.md)