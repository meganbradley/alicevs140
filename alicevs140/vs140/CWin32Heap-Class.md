---
title: "CWin32Heap Class"
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
ms.topic: reference
ms.assetid: 69176022-ed98-4e3b-96d8-116b0c58ac95
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWin32Heap Class
This class implements [IAtlMemMgr](../vs140/IAtlMemMgr-Class.md) using the Win32 heap allocation functions.  
  
> [!IMPORTANT]
>  This class and its members cannot be used in applications that execute in the Windows Runtime.  
  
## Syntax  
  
```  
  
class CWin32Heap : public IAtlMemMgr  
  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CWin32Heap::CWin32Heap](../vs140/CWin32Heap--CWin32Heap.md)|The constructor.|  
|[CWin32Heap::~CWin32Heap](../vs140/CWin32Heap--~CWin32Heap.md)|The destructor.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CWin32Heap::Allocate](../vs140/CWin32Heap--Allocate.md)|Allocates a block of memory from the heap object.|  
|[CWin32Heap::Attach](../vs140/CWin32Heap--Attach.md)|Attaches the heap object to an existing heap.|  
|[CWin32Heap::Detach](../vs140/CWin32Heap--Detach.md)|Detaches the heap object from an existing heap.|  
|[CWin32Heap::Free](../vs140/CWin32Heap--Free.md)|Frees memory previously allocated from the heap.|  
|[CWin32Heap::GetSize](../vs140/CWin32Heap--GetSize.md)|Returns the size of a memory block allocated from the heap object.|  
|[CWin32Heap::Reallocate](../vs140/CWin32Heap--Reallocate.md)|Reallocates a block of memory from the heap object.|  
  
### Public Data Members  
  
|Name|Description|  
|----------|-----------------|  
|[CWin32Heap::m_bOwnHeap](../vs140/CWin32Heap--m_bOwnHeap.md)|A flag used to determine current ownership of the heap handle.|  
|[CWin32Heap::m_hHeap](../vs140/CWin32Heap--m_hHeap.md)|Handle to the heap object.|  
  
## Remarks  
 `CWin32Heap` implements memory allocation methods using the Win32 heap allocation functions, including [HeapAlloc](http://msdn.microsoft.com/library/windows/desktop/aa366597) and [HeapFree](http://msdn.microsoft.com/library/windows/desktop/aa366701). Unlike other Heap classes, `CWin32Heap` requires a valid heap handle to be provided before memory is allocated: the other classes default to using the process heap. The handle can be supplied to the constructor or to the [CWin32Heap::Attach](../vs140/CWin32Heap--Attach.md) method. See the [CWin32Heap::CWin32Heap](../vs140/CWin32Heap--CWin32Heap.md) method for more details.  
  
## Example  
 See the example for [IAtlMemMgr](../vs140/IAtlMemMgr-Class.md).  
  
## Inheritance Hierarchy  
 `IAtlMemMgr`  
  
 `CWin32Heap`  
  
## Requirements  
 **Header:** atlmem.h  
  
##  <a name="cwin32heap__allocate"></a>  CWin32Heap::Allocate  
 Allocates a block of memory from the heap object.  
  
```  
  
virtual __declspec(allocator) void* Allocate(  
      size_t  nBytes  
   ) throw( );  
  
```  
  
### Parameters  
 `nBytes`  
 The requested number of bytes in the new memory block.  
  
### Return Value  
 Returns a pointer to the newly allocated memory block.  
  
### Remarks  
 Call [CWin32Heap::Free](../vs140/CWin32Heap--Free.md) or [CWin32Heap::Reallocate](../vs140/CWin32Heap--Reallocate.md) to free the memory allocated by this method.  
  
 Implemented using [HeapAlloc](http://msdn.microsoft.com/library/windows/desktop/aa366597).  
  
##  <a name="cwin32heap__attach"></a>  CWin32Heap::Attach  
 Attaches the heap object to an existing heap.  
  
```  
  
void Attach(  
      HANDLE  hHeap,  
      bool  bTakeOwnership  
   ) throw( );  
  
```  
  
### Parameters  
 `hHeap`  
 An existing heap handle.  
  
 `bTakeOwnership`  
 A flag indicating if the `CWin32Heap` object is to take ownership over the resources of the heap.  
  
### Remarks  
 If `bTakeOwnership` is TRUE, the `CWin32Heap` object is responsible for deleting the heap handle.  
  
##  <a name="cwin32heap__cwin32heap"></a>  CWin32Heap::CWin32Heap  
 The constructor.  
  
```  
  
CWin32Heap( ) throw( );   
   CWin32Heap(  
      HANDLE  hHeap  
   ) throw( );  
   CWin32Heap(  
      DWORD  dwFlags,  
      size_t  nInitialSize,  
      size_t  nMaxSize  
    = 0   
   );  
  
```  
  
### Parameters  
 `hHeap`  
 An existing heap object.  
  
 `dwFlags`  
 Flags used in creating the heap.  
  
 *nInitialSize*  
 The initial size of the heap.  
  
 `nMaxSize`  
 The maximum size of the heap.  
  
### Remarks  
 Before allocating memory, it is necessary to provide the `CWin32Heap` object with a valid heap handle. The simplest way to achieve this is to use the process heap:  
  
 [!CODE [NVC_ATL_Utilities#92](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#92)]  
  
 It is also possible to supply an existing heap handle to the constructor, in which case the new object does not take over ownership of the heap. The original heap handle will still be valid when the `CWin32Heap` object is deleted.  
  
 An existing heap can also be attached to the new object, using [CWin32Heap::Attach](../vs140/CWin32Heap--Attach.md).  
  
 If a heap is required where operations are all performed from a single thread, the best way is to create the object as follows:  
  
 [!CODE [NVC_ATL_Utilities#93](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#93)]  
  
 The parameter **HEAP_NO_SERIALIZE** specifies that mutual exclusion will not be used when the heap functions allocate and free memory, with an according increase in performance.  
  
 The third parameter defaults to 0, which allows the heap to grow as required. See [HeapCreate](http://msdn.microsoft.com/library/windows/desktop/aa366599\(v=vs.85\).aspx) for an explanation of the memory sizes and flags.  
  
##  <a name="cwin32heap___dtorcwin32heap"></a>  CWin32Heap::~CWin32Heap  
 The destructor.  
  
```  
  
~CWin32Heap( ) throw( );  
  
```  
  
### Remarks  
 Destroys the heap handle if the `CWin32Heap` object has ownership of the heap.  
  
##  <a name="cwin32heap__detach"></a>  CWin32Heap::Detach  
 Detaches the heap object from an existing heap.  
  
```  
  
HANDLE Detach( ) throw( );  
  
```  
  
### Return Value  
 Returns the handle to the heap to which the object was previously attached.  
  
##  <a name="cwin32heap__free"></a>  CWin32Heap::Free  
 Frees memory previously allocated from the heap by [CWin32Heap::Allocate](../vs140/CWin32Heap--Allocate.md) or [CWin32Heap::Reallocate](../vs140/CWin32Heap--Reallocate.md).  
  
```  
  
virtual void Free(  
      void*  p  
   ) throw( );  
  
```  
  
### Parameters  
 `p`  
 Pointer to the block of memory to free. NULL is a valid value and does nothing.  
  
##  <a name="cwin32heap__getsize"></a>  CWin32Heap::GetSize  
 Returns the size of a memory block allocated from the heap object.  
  
```  
  
virtual size_t GetSize(  
      void*  p  
   ) throw( );  
  
```  
  
### Parameters  
 `p`  
 Pointer to the memory block whose size the method will obtain. This is a pointer returned by [CWin32Heap::Allocate](../vs140/CWin32Heap--Allocate.md) or [CWin32Heap::Reallocate](../vs140/CWin32Heap--Reallocate.md).  
  
### Return Value  
 Returns the size, in bytes, of the allocated memory block.  
  
##  <a name="cwin32heap__m_bownheap"></a>  CWin32Heap::m_bOwnHeap  
 A flag used to determine current ownership of the heap handle stored in [m_hHeap](../vs140/CWin32Heap--m_hHeap.md).  
  
```  
  
bool m_bOwnHeap;  
  
```  
  
##  <a name="cwin32heap__m_hheap"></a>  CWin32Heap::m_hHeap  
 Handle to the heap object.  
  
```  
  
HANDLE m_hHeap;  
  
```  
  
### Remarks  
 A variable used to store a handle to the heap object.  
  
##  <a name="cwin32heap__reallocate"></a>  CWin32Heap::Reallocate  
 Reallocates a block of memory from the heap object.  
  
```  
  
virtual __declspec(allocator) void* Reallocate(  
      void*  p,  
      size_t  nBytes  
   ) throw( );  
  
```  
  
### Parameters  
 `p`  
 Pointer to the block of memory to reallocate.  
  
 `nBytes`  
 The new size in bytes of the allocated block. The block can be made larger or smaller.  
  
### Return Value  
 Returns a pointer to the newly allocated memory block.  
  
### Remarks  
 If `p` is NULL, it's assumed that the memory block has not yet been allocated and [CWin32Heap::Allocate](../vs140/CWin32Heap--Allocate.md) is called, with an argument of `nBytes`.  
  
## See Also  
 [Class Overview](../vs140/ATL-Class-Overview.md)   
 [IAtlMemMgr Class](../vs140/IAtlMemMgr-Class.md)   
 [CLocalHeap Class](../vs140/CLocalHeap-Class.md)   
 [CGlobalHeap Class](../vs140/CGlobalHeap-Class.md)   
 [CCRTHeap Class](../vs140/CCRTHeap-Class.md)   
 [CComHeap Class](../vs140/CComHeap-Class.md)