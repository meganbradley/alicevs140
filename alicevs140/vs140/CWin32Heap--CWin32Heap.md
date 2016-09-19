---
title: "CWin32Heap::CWin32Heap"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: 399d1833-508e-4fb8-b5e7-e029473607b0
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWin32Heap::CWin32Heap
The constructor.  
  
## Syntax  
  
```  
  
      CWin32Heap( ) throw( );   
CWin32Heap(  
   HANDLE hHeap   
) throw( );  
CWin32Heap(  
   DWORD dwFlags,  
   size_t nInitialSize,  
   size_t nMaxSize = 0   
);  
```  
  
#### Parameters  
 `hHeap`  
 An existing heap object.  
  
 `dwFlags`  
 Flags used in creating the heap.  
  
 *nInitialSize*  
 The initial size of the heap.  
  
 `nMaxSize`  
 The maximum size of the heap.  
  
## Remarks  
 Before allocating memory, it is necessary to provide the `CWin32Heap` object with a valid heap handle. The simplest way to achieve this is to use the process heap:  
  
 [!CODE [NVC_ATL_Utilities#92](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#92)]  
  
 It is also possible to supply an existing heap handle to the constructor, in which case the new object does not take over ownership of the heap. The original heap handle will still be valid when the `CWin32Heap` object is deleted.  
  
 An existing heap can also be attached to the new object, using [CWin32Heap::Attach](../vs140/CWin32Heap--Attach.md).  
  
 If a heap is required where operations are all performed from a single thread, the best way is to create the object as follows:  
  
 [!CODE [NVC_ATL_Utilities#93](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#93)]  
  
 The parameter **HEAP_NO_SERIALIZE** specifies that mutual exclusion will not be used when the heap functions allocate and free memory, with an according increase in performance.  
  
 The third parameter defaults to 0, which allows the heap to grow as required. See [HeapCreate](http://msdn.microsoft.com/library/windows/desktop/aa366599\(v=vs.85\).aspx) for an explanation of the memory sizes and flags.  
  
## Requirements  
 **Header:** atlmem.h  
  
## See Also  
 [HeapCreate](http://msdn.microsoft.com/library/windows/desktop/aa366599\(v=vs.85\).aspx)