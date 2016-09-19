---
title: "CMemFile Class"
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
ms.assetid: 20e86515-e465-4f73-b2ea-e49789d63165
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMemFile Class
The [CFile](../vs140/CFile-Class.md)-derived class that supports memory files.  
  
## Syntax  
  
```  
class CMemFile : public CFile  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CMemFile::CMemFile](#cmemfile__cmemfile)|Constructs a memory file object.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CMemFile::Attach](#cmemfile__attach)|Attaches a block of memory to `CMemFile`.|  
|[CMemFile::Detach](#cmemfile__detach)|Detaches the block of memory from `CMemFile` and returns a pointer to the block of memory detached.|  
  
### Protected Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CMemFile::Alloc](#cmemfile__alloc)|Override to modify memory allocation behavior.|  
|[CMemFile::Free](#cmemfile__free)|Override to modify memory deallocation behavior.|  
|[CMemFile::GrowFile](#cmemfile__growfile)|Override to modify behavior when growing a file.|  
|[CMemFile::Memcpy](#cmemfile__memcpy)|Override to modify memory copy behavior when reading and writing files.|  
|[CMemFile::Realloc](#cmemfile__realloc)|Override to modify memory reallocation behavior.|  
  
## Remarks  
 These memory files behave like disk files except that the file is stored in RAM rather than on disk. A memory file is useful for fast temporary storage or for transferring raw bytes or serialized objects between independent processes.  
  
 `CMemFile` objects can automatically allocate their own memory or you can attach your own memory block to the `CMemFile` object by calling [Attach](#cmemfile__attach). In either case, memory for growing the memory file automatically is allocated in `nGrowBytes`-sized increments if `nGrowBytes` is not zero.  
  
 The memory block will automatically be deleted upon destruction of the `CMemFile` object if the memory was originally allocated by the `CMemFile` object; otherwise, you are responsible for deallocating the memory you attached to the object.  
  
 You can access the memory block through the pointer supplied when you detach it from the `CMemFile` object by calling [Detach](#cmemfile__detach).  
  
 The most common use of `CMemFile` is to create a `CMemFile` object and use it by calling [CFile](../vs140/CFile-Class.md) member functions. Note that creating a `CMemFile` automatically opens it: you do not call [CFile::Open](../vs140/CFile-Class.md#cfile__open), which is only used for disk files. Because `CMemFile` doesn't use a disk file, the data member `CFile::m_hFile` is not used and has no meaning.  
  
 The `CFile` member functions [Duplicate](../vs140/CFile-Class.md#cfile__duplicate), [LockRange](../vs140/CFile-Class.md#cfile__lockrange), and [UnlockRange](../vs140/CFile-Class.md#cfile__unlockrange) are not implemented for `CMemFile`. If you call these functions on a `CMemFile` object, you will get a [CNotSupportedException](../vs140/CNotSupportedException-Class.md).  
  
 `CMemFile` uses the run-time library functions [malloc](../vs140/malloc.md), [realloc](../vs140/realloc.md), and [free](../vs140/free.md) to allocate, reallocate, and deallocate memory; and the intrinsic [memcpy](../vs140/memcpy--wmemcpy.md) to block copy memory when reading and writing. If you'd like to change this behavior or the behavior when `CMemFile` grows a file, derive your own class from `CMemFile` and override the appropriate functions.  
  
 For more information on `CMemFile`, see the articles [Files in MFC](../vs140/Files-in-MFC.md) and [Memory Management (MFC)](../vs140/Memory-Management.md) and see [File Handling](../Topic/File%20Handling.md) in the                 *Run-Time Library Reference*.  
  
## Inheritance Hierarchy  
 [CObject](../vs140/CObject-Class.md)  
  
 [CFile](../vs140/CFile-Class.md)  
  
 `CMemFile`  
  
## Requirements  
 **Header:** afx.h  
  
##  <a name="cmemfile__alloc"></a>  CMemFile::Alloc  
 This function is called by `CMemFile` member functions.  
  
```  
virtual BYTE* Alloc(    SIZE_T  nBytes );  
  
```  
  
### Parameters  
 `nBytes`  
 Number of bytes of memory to be allocated.  
  
### Return Value  
 A pointer to the memory block that was allocated, or **NULL** if the allocation failed.  
  
### Remarks  
 Override this function to implement custom memory allocation. If you override this function, you'll probably want to override [Free](#cmemfile__free) and [Realloc](#cmemfile__realloc) as well.  
  
 The default implementation uses the run-time library function [malloc](../vs140/malloc.md) to allocate memory.  
  
##  <a name="cmemfile__attach"></a>  CMemFile::Attach  
 Call this function to attach a block of memory to `CMemFile`.  
  
```  
void Attach(    BYTE*  lpBuffer ,    UINT  nBufferSize ,    UINT  nGrowBytes  = 0  );  
  
```  
  
### Parameters  
 `lpBuffer`  
 Pointer to the buffer to be attached to `CMemFile`.  
  
 `nBufferSize`  
 An integer that specifies the size of the buffer in bytes.  
  
 `nGrowBytes`  
 The memory allocation increment in bytes.  
  
### Remarks  
 This causes `CMemFile` to use the block of memory as the memory file.  
  
 If `nGrowBytes` is 0, `CMemFile` will set the file length to `nBufferSize`. This means that the data in the memory block before it was attached to `CMemFile` will be used as the file. Memory files created in this manner cannot be grown.  
  
 Since the file cannot be grown, be careful not to cause `CMemFile` to attempt to grow the file. For example, don't call the `CMemFile` overrides of [CFile:Write](../vs140/CFile-Class.md#cfile__write) to write past the end or don't call [CFile:SetLength](../vs140/CFile-Class.md#cfile__setlength) with a length longer than `nBufferSize`.  
  
 If `nGrowBytes` is greater than 0, `CMemFile` will ignore the contents of the memory block you've attached. You'll have to write the contents of the memory file from scratch using the `CMemFile` override of `CFile::Write`. If you attempt to write past the end of the file or grow the file by calling the `CMemFile` override of `CFile::SetLength`, `CMemFile` will grow the memory allocation in increments of `nGrowBytes`. Growing the memory allocation will fail if the memory block you pass to **Attach** wasn't allocated with a method compatible with [Alloc](#cmemfile__alloc). To be compatible with the default implementation of `Alloc`, you must allocate the memory with the run-time library function [malloc](../vs140/malloc.md) or [calloc](../vs140/calloc.md).  
  
##  <a name="cmemfile__cmemfile"></a>  CMemFile::CMemFile  
 The first overload opens an empty memory file.  
  
```  
CMemFile(    UINT nGrowBytes = 1024 ); CMemFile(    BYTE*  lpBuffer ,    UINT  nBufferSize ,    UINT  nGrowBytes  = 0  );  
  
```  
  
### Parameters  
 `nGrowBytes`  
 The memory allocation increment in bytes.  
  
 *lpBuffe*r  
 Pointer to a buffer that receives information of the size `nBufferSize`.  
  
 `nBufferSize`  
 An integer that specifies the size of the file buffer, in bytes.  
  
### Remarks  
 Note that the file is opened by the constructor and that you should not call [CFile::Open](../vs140/CFile-Class.md#cfile__open).  
  
 The second overload acts the same as if you used the first constructor and immediately called [Attach](#cmemfile__attach) with the same parameters. See **Attach** for details.  
  
### Example  
 [!CODE [NVC_MFCFiles#36](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCFiles#36)]  
  
##  <a name="cmemfile__detach"></a>  CMemFile::Detach  
 Call this function to get a pointer to the memory block being used by `CMemFile`.  
  
```  
BYTE * Detach( );  
  
```  
  
### Return Value  
 A pointer to the memory block that contains the contents of the memory file.  
  
### Remarks  
 Calling this function also closes the `CMemFile`. You can reattach the memory block to `CMemFile` by calling [Attach](#cmemfile__attach). If you want to reattach the file and use the data in it, you should call [CFile::GetLength](../vs140/CFile-Class.md#cfile__getlength) to get the length of the file before calling **Detach**. Note that if you attach a memory block to `CMemFile` so that you can use its data ( `nGrowBytes` == 0), then you won't be able to grow the memory file.  
  
##  <a name="cmemfile__free"></a>  CMemFile::Free  
 This function is called by `CMemFile` member functions.  
  
```  
virtual void Free(    BYTE * lpMem );  
  
```  
  
### Parameters  
 `lpMem`  
 Pointer to the memory to be deallocated                                *.*  
  
### Remarks  
 Override this function to implement custom memory deallocation. If you override this function, you'll probably want to override [Alloc](#cmemfile__alloc) and [Realloc](#cmemfile__realloc) as well.  
  
##  <a name="cmemfile__growfile"></a>  CMemFile::GrowFile  
 This function is called by several of the `CMemFile` member functions.  
  
```  
virtual void GrowFile(    SIZE_T  dwNewLen );  
  
```  
  
### Parameters  
 `dwNewLen`  
 New size of the memory file.  
  
### Remarks  
 You can override it if you want to change how `CMemFile` grows its file. The default implementation calls [Realloc](#cmemfile__realloc) to grow an existing block (or [Alloc](#cmemfile__alloc) to create a memory block), allocating memory in multiples of the `nGrowBytes` value specified in the constructor or [Attach](#cmemfile__attach) call.  
  
##  <a name="cmemfile__memcpy"></a>  CMemFile::Memcpy  
 This function is called by the `CMemFile` overrides of [CFile::Read](../vs140/CFile-Class.md#cfile__read) and [CFile::Write](../vs140/CFile-Class.md#cfile__write) to transfer data to and from the memory file.  
  
```  
virtual BYTE* Memcpy(    BYTE*  lpMemTarget ,    const BYTE*  lpMemSource ,    SIZE_T  nBytes );  
  
```  
  
### Parameters  
 `lpMemTarget`  
 Pointer to the memory block into which the source memory will be copied.  
  
 `lpMemSource`  
 Pointer to the source memory block.  
  
 `nBytes`  
 Number of bytes to be copied.  
  
### Return Value  
 A copy of `lpMemTarget`.  
  
### Remarks  
 Override this function if you want to change the way that `CMemFile` does these memory copies.  
  
##  <a name="cmemfile__realloc"></a>  CMemFile::Realloc  
 This function is called by `CMemFile` member functions.  
  
```  
virtual BYTE* Realloc(    BYTE*  lpMem ,    SIZE_T  nBytes );  
  
```  
  
### Parameters  
 `lpMem`  
 A pointer to the memory block to be reallocated.  
  
 `nBytes`  
 New size for the memory block.  
  
### Return Value  
 A pointer to the memory block that was reallocated (and possibly moved), or **NULL** if the reallocation failed.  
  
### Remarks  
 Override this function to implement custom memory reallocation. If you override this function, you'll probably want to override [Alloc](#cmemfile__alloc) and [Free](#cmemfile__free) as well.  
  
## See Also  
 [Base Class](../vs140/CFile-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)