---
title: "CGlobalHeap Class"
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
ms.assetid: e348d838-3aa7-4bee-a1b3-cd000c99f834
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CGlobalHeap Class
This class implements             [IAtlMemMgr](../vs140/IAtlMemMgr-Class.md) using the Win32 global heap functions.  
  
> [!IMPORTANT]
>  This class and its members cannot be used in applications that execute in the Windows Runtime.  
  
## Syntax  
  
```  
  
class CGlobalHeap : public IAtlMemMgr  
  
```  
  
## Members  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CGlobalHeap::Allocate](../vs140/CGlobalHeap--Allocate.md)|Call this method to allocate a block of memory.|  
|[CGlobalHeap::Free](../vs140/CGlobalHeap--Free.md)|Call this method to free a block of memory allocated by this memory manager.|  
|[CGlobalHeap::GetSize](../vs140/CGlobalHeap--GetSize.md)|Call this method to get the allocated size of a memory block allocated by this memory manager.|  
|[CGlobalHeap::Reallocate](../vs140/CGlobalHeap--Reallocate.md)|Call this method to reallocate memory allocated by this memory manager.|  
  
## Remarks  
 `CGlobalHeap` implements memory allocation functions using the Win32 global heap functions.  
  
> [!NOTE]
>  The global heap functions are slower than other memory management functions and do not provide as many features. Therefore, new applications should use the                     [heap functions](http://msdn.microsoft.com/library/windows/desktop/aa366711). These are available in the                     [CWin32Heap](../vs140/CWin32Heap-Class.md) class. Global functions are still used by DDE and the clipboard functions.  
  
## Example  
 See the example for                     [IAtlMemMgr](../vs140/IAtlMemMgr-Class.md).  
  
## Inheritance Hierarchy  
 `IAtlMemMgr`  
  
 `CGlobalHeap`  
  
## Requirements  
 **Header:** atlmem.h  
  
##  <a name="cglobalheap__allocate"></a>  CGlobalHeap::Allocate  
 Call this method to allocate a block of memory.  
  
```  
  
virtual __declspec(allocator) void* Allocate(  
   size_t   
nBytes  
) throw( );  
  
```  
  
### Parameters  
 `nBytes`  
 The requested number of bytes in the new memory block.  
  
### Return Value  
 Returns a pointer to the start of the newly allocated memory block.  
  
### Remarks  
 Call                         [CGlobalHeap::Free](../vs140/CGlobalHeap--Free.md) or                         [CGlobalHeap::Reallocate](../vs140/CGlobalHeap--Reallocate.md) to free the memory allocated by this method.  
  
 Implemented using                         [GlobalAlloc](http://msdn.microsoft.com/library/windows/desktop/aa366574) with a flag parameter of                         **GMEM_FIXED**.  
  
##  <a name="cglobalheap__free"></a>  CGlobalHeap::Free  
 Call this method to free a block of memory allocated by this memory manager.  
  
```  
  
virtual void Free(  
   void*   
p  
) throw( );  
  
```  
  
### Parameters  
 `p`  
 Pointer to memory previously allocated by this memory manager. NULL is a valid value and does nothing.  
  
### Remarks  
 Implemented using                         [GlobalFree](http://msdn.microsoft.com/library/windows/desktop/aa366579).  
  
##  <a name="cglobalheap__getsize"></a>  CGlobalHeap::GetSize  
 Call this method to get the allocated size of a memory block allocated by this memory manager.  
  
```  
  
virtual size_t GetSize(  
   void*   
p  
) throw( );  
  
```  
  
### Parameters  
 `p`  
 Pointer to memory previously allocated by this memory manager.  
  
### Return Value  
 Returns the size of the allocated memory block in bytes.  
  
### Remarks  
 Implemented using                         [GlobalSize](http://msdn.microsoft.com/library/windows/desktop/aa366593).  
  
##  <a name="cglobalheap__reallocate"></a>  CGlobalHeap::Reallocate  
 Call this method to reallocate memory allocated by this memory manager.  
  
```  
  
virtual __declspec(allocator) void* Reallocate(  
   void*   
p  
,  
   size_t   
nBytes  
) throw( );  
  
```  
  
### Parameters  
 `p`  
 Pointer to memory previously allocated by this memory manager.  
  
 `nBytes`  
 The requested number of bytes in the new memory block.  
  
### Return Value  
 Returns a pointer to the start of the newly allocated memory block.  
  
### Remarks  
 Call                         [CGlobalHeap::Free](../vs140/CGlobalHeap--Free.md) to free the memory allocated by this method.  
  
 Implemented using                         [GlobalReAlloc](http://msdn.microsoft.com/library/windows/desktop/aa366590).  
  
## See Also  
 [Class Overview](../vs140/ATL-Class-Overview.md)   
 [CComHeap Class](../vs140/CComHeap-Class.md)   
 [CWin32Heap Class](../vs140/CWin32Heap-Class.md)   
 [CLocalHeap Class](../vs140/CLocalHeap-Class.md)   
 [CCRTHeap Class](../vs140/CCRTHeap-Class.md)   
 [IAtlMemMgr Class](../vs140/IAtlMemMgr-Class.md)