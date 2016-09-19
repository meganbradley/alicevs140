---
title: "How to: Create and Use unique_ptr Instances"
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
ms.assetid: 9a373030-e587-452f-b9a5-c5f9d58b7673
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Create and Use unique_ptr Instances
A [unique_ptr](../vs140/unique_ptr-Class.md) does not share its pointer. It cannot be copied to another `unique_ptr`, passed by value to a function, or used in any Standard Template Library (STL) algorithm that requires copies to be made. A `unique_ptr` can only be moved. This means that the ownership of the memory resource is transferred to another `unique_ptr` and the original `unique_ptr` no longer owns it. We recommend that you restrict an object to one owner, because multiple ownership adds complexity to the program logic. Therefore, when you need a smart pointer for a plain C++ object, use `unique_ptr`, and when you construct a `unique_ptr`, use the [make_unique](../vs140/make_unique.md) helper function.  
  
 The following diagram illustrates the transfer of ownership between two `unique_ptr` instances.  
  
 ![Moving the ownership of a unique&#95;ptr](../vs140/media/unique_ptr.png "unique_ptr")  
  
 `unique_ptr` is defined in the `<memory>` header in the STL. It is exactly is efficient as a raw pointer and can be used in STL containers. The addition of `unique_ptr` instances to STL containers is efficient because the move constructor of the `unique_ptr` eliminates the need for a copy operation.  
  
## Example  
 The following example shows how to create `unique_ptr` instances and pass them between functions.  
  
 [!CODE [stl_smart_pointers#210](../CodeSnippet/VS_Snippets_Cpp/stl_smart_pointers#210)]  
  
 These examples demonstrate this basic characteristic of `unique_ptr`: it can be moved, but not copied. "Moving" transfers ownership to a new `unique_ptr` and resets the old `unique_ptr`.  
  
## Example  
 The following example shows how to create `unique_ptr` instances and use them in a vector.  
  
 [!CODE [stl_smart_pointers#211](../CodeSnippet/VS_Snippets_Cpp/stl_smart_pointers#211)]  
  
 In the range for  loop, notice that the `unique_ptr` is passed by reference. If you try to pass by value here, the compiler will throw an error because the `unique_ptr` copy constructor is deleted.  
  
## Example  
 The following example shows how to initialize a `unique_ptr` that is a class member.  
  
 [!CODE [stl_smart_pointers#212](../CodeSnippet/VS_Snippets_Cpp/stl_smart_pointers#212)]  
  
## Example  
 You can use [make_unique](../vs140/make_unique.md) to create a `unique_ptr` to an array, but you cannot use `make_unique` to initialize the array elements.  
  
 [!CODE [stl_smart_pointers#213](../CodeSnippet/VS_Snippets_Cpp/stl_smart_pointers#213)]  
  
 For more examples, see [make_unique](../vs140/make_unique.md).  
  
## See Also  
 [Smart Pointers](../vs140/Smart-Pointers--Modern-C---.md)   
 [make_unique](../vs140/make_unique.md)