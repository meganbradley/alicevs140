---
title: "Smart Pointers (Modern C++)"
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
ms.assetid: 909ef870-904c-49b6-b8cd-e9d0b7dc9435
caps.latest.revision: 28
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Smart Pointers (Modern C++)
In modern C++ programming, the Standard Library includes *smart pointers*, which are used to help ensure that programs are free of memory and resource leaks and are exception-safe.  
  
## Uses for smart pointers  
 Smart pointers are defined in the `std` namespace in the [<memory\>](../vs140/-memory-.md) header file. They are crucial to the [RAII](../vs140/Objects-Own-Resources--RAII-.md) or *Resource Acquisition Is Initialialization* programming idiom. The main goal of this idiom is to ensure that resource acquisition occurs at the same time that the object is initialized, so that all resources for the object are created and made ready in one line of code. In practical terms, the main principle of RAII is to give ownership of any heap-allocated resource—for example, dynamically-allocated memory or system object handles—to a stack-allocated object whose destructor contains the code to delete or free the resource and also any associated cleanup code.  
  
 In most cases, when you initialize a raw pointer or resource handle to point to an actual resource, pass the pointer to a smart pointer immediately. In modern C++, raw pointers are only used in small code blocks of limited scope, loops, or helper functions where performance is critical and there is no chance of confusion about ownership.  
  
 The following example compares a raw pointer declaration to a smart pointer declaration.  
  
 [!CODE [smart_pointers_intro#1](../CodeSnippet/VS_Snippets_Cpp/smart_pointers_intro#1)]  
  
 As shown in the example, a smart pointer is a class template that you declare on the stack, and initialize by using a raw pointer that points to a heap-allocated object. After the smart pointer is initialized, it owns the raw pointer. This means that the smart pointer is responsible for deleting the memory that the raw pointer specifies. The smart pointer destructor contains the call to delete, and because the smart pointer is declared on the stack, its destructor is invoked when the smart pointer goes out of scope, even if an exception is thrown somewhere further up the stack.  
  
 Access the encapsulated pointer by using the familiar pointer operators, `->` and `*`, which the smart pointer class overloads to return the encapsulated raw pointer.  
  
 The C++ smart pointer idiom resembles object creation in languages such as C#: you create the object and then let the system take care of deleting it at the correct time. The difference is that no separate garbage collector runs in the background; memory is managed through the standard C++ scoping rules so that the runtime environment is faster and more efficient.  
  
> [!IMPORTANT]
>  Always create smart pointers on a separate line of code, never in a parameter list, so that a subtle resource leak won't occur due to certain parameter list allocation rules.  
  
 The following example shows how a `unique_ptr` smart pointer type from the Standard Template Library could be used to encapsulate a pointer to a large object.  
  
 [!CODE [smart_pointers_intro#2](../CodeSnippet/VS_Snippets_Cpp/smart_pointers_intro#2)]  
  
 The example demonstrates the following essential steps for using smart pointers.  
  
1.  Declare the smart pointer as an automatic (local) variable. (Do not use the `new` or `malloc` expression on the smart pointer itself.)  
  
2.  In the type parameter, specify the pointed-to type of the encapsulated pointer.  
  
3.  Pass a raw pointer to a `new`-ed object in the smart pointer constructor. (Some utility functions or smart pointer constructors do this for you.)  
  
4.  Use the overloaded `->` and `*` operators to access the object.  
  
5.  Let the smart pointer delete the object.  
  
 Smart pointers are designed to be as efficient as possible both in terms of memory and performance. For example, the only data member in `unique_ptr` is the encapsulated pointer. This means that `unique_ptr` is exactly the same size as that pointer, either four bytes or eight bytes. Accessing the encapsulated pointer by using the smart pointer overloaded * and -> operators is not significantly slower than accessing the raw pointers directly.  
  
 Smart pointers have their own member functions, which are accessed by using “dot” notation. For example, some STL smart pointers have a reset member function that releases ownership of the pointer. This is useful when you want to free the memory owned by the smart pointer before the smart pointer goes out of scope, as shown in the following example.  
  
 [!CODE [smart_pointers_intro#3](../CodeSnippet/VS_Snippets_Cpp/smart_pointers_intro#3)]  
  
 Smart pointers usually provide a way to access their  raw pointer directly. STL smart pointers have a `get` member function for this purpose, and `CComPtr` has a public `p` class member. By providing direct access to the underlying pointer, you can use the smart pointer to manage memory in your own code and still pass the raw pointer to code that does not support smart pointers.  
  
 [!CODE [smart_pointers_intro#4](../CodeSnippet/VS_Snippets_Cpp/smart_pointers_intro#4)]  
  
## Kinds of Smart Pointers  
 The following section summarizes the different kinds of smart pointers that are available in the Windows programming environment and describes when to use them.  
  
 **C++ Standard Library Smart Pointers**  
 Use these smart pointers as a first choice for encapsulating pointers to plain old C++ objects (POCO).  
  
-   `unique_ptr`   
     Allows exactly one owner of the underlying pointer. Use as the default choice for POCO unless you know for certain that you require a `shared_ptr`. Can be moved to a new owner, but not copied or shared. Replaces `auto_ptr`, which is deprecated. Compare to `boost::scoped_ptr`. `unique_ptr` is small and efficient; the size is one pointer and it supports rvalue references for fast insertion and retrieval from STL collections. Header file: `<memory>`. For more information, see [How to: Create and use unique_ptr instances](../vs140/How-to--Create-and-Use-unique_ptr-Instances.md) and [unique_ptr Class](../vs140/unique_ptr-Class.md).  
  
-   `shared_ptr`   
     Reference-counted smart pointer. Use when you want to assign one raw pointer to multiple owners, for example, when you return a copy of a pointer from a container but want to keep the original. The raw pointer is not deleted until all `shared_ptr` owners have gone out of scope or have otherwise given up ownership. The size is two pointers; one for the object and one for the shared control block that contains the reference count. Header file: `<memory>`. For more information, see [How to: Create and Use shared_ptr Instances](../vs140/How-to--Create-and-Use-shared_ptr-Instances.md) and [shared_ptr Class](../vs140/shared_ptr-Class.md).  
  
-   `weak_ptr`   
    Special-case smart pointer for use in conjunction with `shared_ptr`. A `weak_ptr` provides access to an object that is owned by one or more `shared_ptr` instances, but does not participate in reference counting. Use when you want to observe an object, but do not require it to remain alive. Required in some cases to break circular references between `shared_ptr` instances. Header file: `<memory>`. For more information, see [How to: Create and Use weak_ptr Instances](../vs140/How-to--Create-and-Use-weak_ptr-Instances.md) and [weak_ptr Class](../vs140/weak_ptr-Class.md).  
  
 **Smart Pointers for COM Objects (Classic Windows Programming)**  
 When you work with COM objects, wrap the interface pointers in an appropriate smart pointer type. The Active Template Library (ATL) defines several smart pointers for various purposes. You can also use the `_com_ptr_t` smart pointer type, which the compiler uses when it creates wrapper classes from .tlb files. It's the best choice when you do not want to include the ATL header files.  
  
 [CComPtr Class](../vs140/CComPtr-Class.md)  
 Use this unless you cannot use ATL. Performs reference counting by using the `AddRef` and `Release` methods. For more information, see [How to: Create and Use CComPtr and CComQIPtr Instances](../vs140/How-to--Create-and-Use-CComPtr-and-CComQIPtr-Instances.md).  
  
 [CComQIPtr Class](../vs140/CComQIPtr-Class.md)  
 Resembles `CComPtr` but also provides simplified syntax for calling `QueryInterface` on COM objects. For more information, see [How to: Create and Use CComPtr and CComQIPtr Instances](../vs140/How-to--Create-and-Use-CComPtr-and-CComQIPtr-Instances.md).  
  
 [CComHeapPtr Class](../vs140/CComHeapPtr-Class.md)  
 Smart pointer to objects that use `CoTaskMemFree` to free memory.  
  
 [CComGITPtr Class](../vs140/CComGITPtr-Class.md)  
 Smart pointer for interfaces that are obtained from the global interface table (GIT).  
  
 [_com_ptr_t Class](../vs140/_com_ptr_t-Class.md)  
 Resembles `CComQIPtr` in functionality but does not depend on ATL headers.  
  
 **ATL Smart Pointers for POCO Objects**  
 In addition to smart pointers for COM objects, ATL also defines smart pointers, and collections of smart pointers, for plain old C++ objects. In classic Windows programming, these types are useful alternatives to the STL collections, especially when code portability is not required or when you do not want to mix the programming models of STL and ATL.  
  
 [CAutoPtr Class](../vs140/CAutoPtr-Class.md)  
 Smart pointer that enforces unique ownership by transferring ownership on copy. Comparable to the deprecated `std::auto_ptr` Class.  
  
 [CHeapPtr Class](../vs140/CHeapPtr-Class.md)  
 Smart pointer for objects that are allocated by using the C [malloc](../vs140/malloc.md) function.  
  
 [CAutoVectorPtr Class](../vs140/CAutoVectorPtr-Class.md)  
 Smart pointer for arrays that are allocated by using `new[]`.  
  
 [CAutoPtrArray Class](../vs140/CAutoPtrArray-Class.md)  
 Class that encapsulates an array of `CAutoPtr` elements.  
  
 [CAutoPtrList Class](../vs140/CAutoPtrList-Class.md)  
 Class that encapsulates methods for manipulating a list of `CAutoPtr` nodes.  
  
## See Also  
 [Welcome Back to C++](../vs140/Welcome-Back-to-C----Modern-C---.md)   
 [C++ Language Reference](../vs140/C---Language-Reference.md)   
 [Standard C++ Library](../vs140/C---Standard-Library-Reference.md)   
 [(NOTINBUILD)Overview: Memory Management in C++](assetId:///2201885d-3d91-4a6e-aaa6-7a554e0362a8)