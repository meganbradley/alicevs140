---
title: "_heapwalk"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
  - C
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
apiname: 
  - _heapwalk
apilocation: 
  - msvcrt.dll
  - msvcr110_clr0400.dll
  - msvcr100.dll
  - msvcr110.dll
  - msvcr80.dll
  - msvcr120.dll
  - msvcr90.dll
apitype: DLLExport
ms.assetid: 2df67649-fb00-4570-a8b1-a4eca5738744
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _heapwalk
Traverses the heap and returns information about the next entry.  
  
> [!IMPORTANT]
>  This API cannot be used in applications that execute in the Windows Runtime except in Debug builds. For more information, see [CRT functions not supported with /ZW](http://msdn.microsoft.com/library/windows/apps/jj606124.aspx).  
  
## Syntax  
  
```  
int _heapwalk(   
   _HEAPINFO *entryinfo   
);  
```  
  
#### Parameters  
 `entryinfo`  
 Buffer to contain heap information.  
  
## Return Value  
 `_heapwalk` returns one of the following integer manifest constants defined in Malloc.h.  
  
 `_HEAPBADBEGIN`  
 Initial header information invalid or not found.  
  
 `_HEAPBADNODE`  
 Heap damaged or bad node found.  
  
 `_HEAPBADPTR`  
 `_pentry` field of the `_HEAPINFO` structure does not contain a valid pointer into the heap or `entryinfo` is a null pointer.  
  
 `_HEAPEND`  
 End of the heap reached successfully.  
  
 `_HEAPEMPTY`  
 Heap not initialized.  
  
 `_HEAPOK`  
 No errors so far; `entryinfo` is updated with information about the next heap entry.  
  
 In addition, if an error occurs, `_heapwalk` sets `errno` to `ENOSYS`.  
  
## Remarks  
 The `_heapwalk` function helps debug heap-related problems in programs. The function walks through the heap, traversing one entry per call, and returns a pointer to a structure of type `_HEAPINFO` that contains information about the next heap entry. The `_HEAPINFO` type, defined in Malloc.h, contains the following elements.  
  
 `int *_pentry`  
 Heap entry pointer.  
  
 `size_t _size`  
 Size of the heap entry.  
  
 `int _useflag`  
 Flag that indicates whether the heap entry is in use.  
  
 A call to `_heapwalk` that returns `_HEAPOK` stores the size of the entry in the `_size` field and sets the `_useflag` field to either `_FREEENTRY` or `_USEDENTRY` (both are constants defined in Malloc.h). To obtain this information about the first entry in the heap, pass `_heapwalk` a pointer to a `_HEAPINFO` structure whose `_pentry` member is `NULL`. If the operating system does not support `_heapwalk`(for example, Windows 98), the function returns `_HEAPEND` and sets `errno` to `ENOSYS`.  
  
 This function validates its parameter. If `entryinfo` is a null pointer, the invalid parameter handler is invoked, as described in [Parameter Validation](../vs140/Parameter-Validation.md). If execution is allowed to continue, `errno` is set to `EINVAL` and the function returns `_HEAPBADPTR`.  
  
## Requirements  
  
|Routine|Required header|Optional header|  
|-------------|---------------------|---------------------|  
|`_heapwalk`|<malloc.h>|<errno.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## Example  
  
```  
// crt_heapwalk.c  
  
// This program "walks" the heap, starting  
// at the beginning (_pentry = NULL). It prints out each  
// heap entry's use, location, and size. It also prints  
// out information about the overall state of the heap as  
// soon as _heapwalk returns a value other than _HEAPOK  
// or if the loop has iterated 100 times.  
  
#include <stdio.h>  
#include <malloc.h>  
  
void heapdump(void);  
  
int main(void)  
{  
    char *buffer;  
  
    heapdump();  
    if((buffer = (char *)malloc(59)) != NULL)  
    {  
        heapdump();  
        free(buffer);  
    }  
    heapdump();  
}  
  
void heapdump(void)  
{  
    _HEAPINFO hinfo;  
    int heapstatus;  
    int numLoops;  
    hinfo._pentry = NULL;  
    numLoops = 0;  
    while((heapstatus = _heapwalk(&hinfo)) == _HEAPOK &&  
          numLoops < 100)  
    {  
        printf("%6s block at %Fp of size %4.4X\n",  
               (hinfo._useflag == _USEDENTRY ? "USED" : "FREE"),  
               hinfo._pentry, hinfo._size);  
        numLoops++;  
    }  
  
    switch(heapstatus)  
    {  
    case _HEAPEMPTY:  
        printf("OK - empty heap\n");  
        break;  
    case _HEAPEND:  
        printf("OK - end of heap\n");  
        break;  
    case _HEAPBADPTR:  
        printf("ERROR - bad pointer to heap\n");  
        break;  
    case _HEAPBADBEGIN:  
        printf("ERROR - bad start of heap\n");  
        break;  
    case _HEAPBADNODE:  
        printf("ERROR - bad node in heap\n");  
        break;  
    }  
}  
```  
  
  **USED block at 00310650 of size 0100**  
 **USED block at 00310758 of size 0800**  
 **USED block at 00310F60 of size 0080**  
 **FREE block at 00310FF0 of size 0398**  
 **USED block at 00311390 of size 000D**  
 **USED block at 003113A8 of size 00B4**  
 **USED block at 00311468 of size 0034**  
 **USED block at 003114A8 of size 0039**  
**...**  
 **USED block at 00312228 of size 0010**  
 **USED block at 00312240 of size 1000**  
 **FREE block at 00313250 of size 1DB0**  
**OK - end of heap**   
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [Memory Allocation](../vs140/Memory-Allocation.md)   
 [_heapadd](../vs140/_heapadd.md)   
 [_heapchk](../vs140/_heapchk.md)   
 [_heapmin](../vs140/_heapmin.md)   
 [_heapset](../vs140/_heapset.md)