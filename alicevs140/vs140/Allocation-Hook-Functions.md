---
title: "Allocation Hook Functions"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - FSharp
  - VB
  - CSharp
  - C++
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6bfbdb65-8cb1-4c21-8c45-7194a2b77c1e
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Allocation Hook Functions
An allocation hook function, installed using [_CrtSetAllocHook](../vs140/_CrtSetAllocHook.md), is called every time memory is allocated, re-allocated, or freed. This type of hook can be used for many different purposes. Use it to test how an application handles insufficient memory situations, for example, or to examine allocation patterns, or to log allocation information for later analysis.  
  
> [!NOTE]
>  Be aware of the restriction about using C run-time library functions in an allocation hook function, described in [Allocation Hooks and C Run-Time Memory Allocations](../vs140/Allocation-Hooks-and-C-Run-Time-Memory-Allocations.md).  
  
 An allocation hook function should have a prototype like the following:  
  
```  
int YourAllocHook(int nAllocType, void *pvData,  
        size_t nSize, int nBlockUse, long lRequest,  
        const unsigned char * szFileName, int nLine )  
```  
  
 The pointer that you pass to [_CrtSetAllocHook](../vs140/_CrtSetAllocHook.md) is of type **_CRT_ALLOC_HOOK**, as defined in CRTDBG.H:  
  
```  
typedef int (__cdecl * _CRT_ALLOC_HOOK)  
    (int, void *, size_t, int, long, const unsigned char *, int);  
```  
  
 When the run-time library calls your hook, the *nAllocType* argument indicates what allocation operation is about to be performed (**_HOOK_ALLOC**, **_HOOK_REALLOC**, or **_HOOK_FREE**). In the case of a free or a reallocation, `pvData` contains a pointer to the user topic of the block about to be freed. However, in the case of an allocation, this pointer is null, because the allocation has not yet occurred. The remaining arguments contain the size of the allocation in question, its block type, the sequential request number associated with it, and a pointer to the file name and line number in which the allocation was made, if available. After the hook function performs whatever analysis and other tasks its author wants, it must return either **TRUE**, indicating that the allocation operation can continue, or **FALSE**, indicating that the operation should fail. A simple hook of this type might check the amount of memory allocated so far, and return **FALSE** if that amount exceeded a small limit. The application would then experience the kind of allocation errors that would normally occur only when available memory was very low. More complex hooks might keep track of allocation patterns, analyze memory use, or report when specific situations occur.  
  
## See Also  
 [Allocation Hooks and C Run-Time Memory Allocations](../vs140/Allocation-Hooks-and-C-Run-Time-Memory-Allocations.md)   
 [Debug Hook Function Writing](../vs140/Debug-Hook-Function-Writing.md)   
 [crt_dbg2 Sample](assetId:///21e1346a-6a17-4f57-b275-c76813089167)