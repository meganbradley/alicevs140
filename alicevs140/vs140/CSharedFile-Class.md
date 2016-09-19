---
title: "CSharedFile Class"
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
ms.assetid: 5d000422-9ede-4318-a8c9-f7412b674f39
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSharedFile Class
The [CMemFile](../vs140/CMemFile-Class.md)-derived class that supports shared memory files.  
  
## Syntax  
  
```  
class CSharedFile : public CMemFile  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CSharedFile::CSharedFile](#csharedfile__csharedfile)|Constructs a `CSharedFile` object.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CSharedFile::Detach](#csharedfile__detach)|Closes the shared memory file and returns the handle of its memory block.|  
|[CSharedFile::SetHandle](#csharedfile__sethandle)|Attaches the shared memory file to a memory block.|  
  
## Remarks  
 Memory files behave like disk files except that the file is stored in RAM rather than on disk. A memory file is useful for fast temporary storage or for transferring raw bytes or serialized objects between independent processes.  
  
 Shared memory files differ from other memory files in that memory for them is allocated with the                 [GlobalAlloc](http://msdn.microsoft.com/library/windows/desktop/aa366574) Windows function. The `CSharedFile` class stores data in a globally allocated memory block (created using **GlobalAlloc**), and this memory block can be shared using DDE, the Clipboard, or other OLE/COM uniform data transfer operations, for example, using `IDataObject`.  
  
 **GlobalAlloc** returns an `HGLOBAL` handle rather than a pointer to memory, such as the pointer returned by [malloc](../vs140/malloc.md). The `HGLOBAL` handle is needed in certain applications. For example, to put data on the Clipboard you need an `HGLOBAL` handle.  
  
 Please note that `CSharedFile` does not use memory-mapped files, and the data cannot be directly shared between processes.  
  
 `CSharedFile` objects can automatically allocate their own memory or you can attach your own memory block to the `CSharedFile` object by calling [CSharedFile::SetHandle](#csharedfile__sethandle). In either case, memory for growing the memory file automatically is allocated in `nGrowBytes`-sized increments if `nGrowBytes` is not zero.  
  
 For more information, see the article [Files in MFC](../vs140/Files-in-MFC.md) and [File Handling](../Topic/File%20Handling.md) in the                 *Run-Time Library Reference*.  
  
## Inheritance Hierarchy  
 [CObject](../vs140/CObject-Class.md)  
  
 [CFile](../vs140/CFile-Class.md)  
  
 [CMemFile](../vs140/CMemFile-Class.md)  
  
 `CSharedFile`  
  
## Requirements  
 **Header:** afxadv.h  
  
##  <a name="csharedfile__csharedfile"></a>  CSharedFile::CSharedFile  
 Constructs a `CSharedFile` object and allocates memory for it.  
  
```  
CSharedFile(    UINT  nAllocFlags  = GMEM_DDESHARE | GMEM_MOVEABLE,    UINT  nGrowBytes  = 4096  );  
  
```  
  
### Parameters  
 *nAllocFlags*  
 Flags indicating how memory is to be allocated. See                                 [GlobalAlloc](http://msdn.microsoft.com/library/windows/desktop/aa366574) for a list of valid flag values.  
  
 `nGrowBytes`  
 The memory allocation increment in bytes.  
  
##  <a name="csharedfile__detach"></a>  CSharedFile::Detach  
 Call this function to close the memory file and detach it from the memory block.  
  
```  
HGLOBAL Detach( );  
  
```  
  
### Return Value  
 The handle of the memory block that contains the contents of the memory file.  
  
### Remarks  
 You can reopen it by calling [SetHandle](#csharedfile__sethandle), using the handle returned by **Detach**.  
  
##  <a name="csharedfile__sethandle"></a>  CSharedFile::SetHandle  
 Call this function to attach a block of global memory to the `CSharedFile` object.  
  
```  
void SetHandle(    HGLOBAL  hGlobalMemory ,    BOOL  bAllowGrow  = TRUE  );  
  
```  
  
### Parameters  
 *hGlobalMemory*  
 Handle to the global memory to be attached to the `CSharedFile`.  
  
 `bAllowGrow`  
 Specifies whether the memory block is allowed to grow.  
  
### Remarks  
 If `bAllowGrow` is nonzero, the size of the memory block is increased as necessary, for example, if an attempt is made to write more bytes to the file than were allocated for the memory block.  
  
## See Also  
 [Base Class](../vs140/CMemFile-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMemFile](../vs140/CMemFile-Class.md)   
 [GlobalAlloc](http://msdn.microsoft.com/library/windows/desktop/aa366574)   
 [GlobalFree](http://msdn.microsoft.com/library/windows/desktop/aa366579)   
 [GlobalRealloc](http://msdn.microsoft.com/library/windows/desktop/aa366590)