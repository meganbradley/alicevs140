---
title: "_CrtReportBlockType"
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
  - _CrtReportBlockType
apilocation: 
  - msvcr110_clr0400.dll
  - msvcr110.dll
  - msvcr90.dll
  - msvcr80.dll
  - msvcrt.dll
  - msvcr100.dll
  - msvcr120.dll
apitype: DLLExport
ms.assetid: 0f4b9da7-bebb-4956-9541-b2581640ec6b
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _CrtReportBlockType
Returns the block type/subtype associated with a given debug heap block pointer.  
  
## Syntax  
  
```  
  
      int _CrtReportBlockType(  
   const void * pBlock  
};  
```  
  
#### Parameters  
 *pBlock*  
 Pointer to a valid debug heap block.  
  
## Return Value  
 When passed a valid debug heap pointer, the `_CrtReportBlockType` function returns the block type and subtype in the form of an `int`. When passed an invalid pointer, the function returns -1.  
  
## Remarks  
 To extract the type and subtype returned by `_CrtReportBlockType`, use the macros **_BLOCK_TYPE** and **_BLOCK_SUBTYPE** (both defined in Crtdbg.h) on the return value.  
  
 For information about the allocation block types and how they are used, see [Types of Blocks on the Debug Heap](../vs140/CRT-Debug-Heap-Details.md#BKMK_Types_of_blocks_on_the_debug_heap).  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_CrtReportBlockType`|<crtdbg.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Libraries  
 Debug versions of [C run-time libraries](../vs140/CRT-Library-Features.md) only.  
  
## Example  
  
```  
// crt_crtreportblocktype.cpp  
// compile with: /MDd  
  
#include <malloc.h>  
#include <stdio.h>  
#include <crtdbg.h>  
  
void __cdecl Dumper(void *ptr, void *)  
{  
    int block = _CrtReportBlockType(ptr);  
    _RPT3(_CRT_WARN, "Dumper found block at %p: type %d, subtype %d\n", ptr,  
          _BLOCK_TYPE(block), _BLOCK_SUBTYPE(block));  
}  
  
void __cdecl LeakDumper(void *ptr, size_t sz)  
{  
    int block = _CrtReportBlockType(ptr);  
    _RPT4(_CRT_WARN, "LeakDumper found block at %p:"  
                     " type %d, subtype %d, size %d\n", ptr,  
          _BLOCK_TYPE(block), _BLOCK_SUBTYPE(block), sz);  
}  
  
int main(void)  
{  
    _CrtSetDbgFlag(_CrtSetDbgFlag(_CRTDBG_REPORT_FLAG) |   
    _CRTDBG_LEAK_CHECK_DF);  
    _CrtSetReportMode( _CRT_WARN, _CRTDBG_MODE_FILE );  
    _CrtSetReportFile( _CRT_WARN, _CRTDBG_FILE_STDOUT );  
    _malloc_dbg(10, _NORMAL_BLOCK , __FILE__, __LINE__);  
    _malloc_dbg(10, _CLIENT_BLOCK | (1 << 16), __FILE__, __LINE__);  
    _malloc_dbg(20, _CLIENT_BLOCK | (2 << 16), __FILE__, __LINE__);  
    _malloc_dbg(30, _CLIENT_BLOCK | (3 << 16), __FILE__, __LINE__);  
    _CrtDoForAllClientObjects(Dumper, NULL);  
    _CrtSetDumpClient(LeakDumper);  
}  
```  
  
## Sample Output  
  
```  
Dumper found block at 00314F78: type 4, subtype 3  
Dumper found block at 00314F38: type 4, subtype 2  
Dumper found block at 00314F00: type 4, subtype 1  
Detected memory leaks!  
Dumping objects ->  
crt_crtreportblocktype.cpp(30) : {55} client block at 0x00314F78, subtype 3, 30 bytes long.  
 Data: <                > CD CD CD CD CD CD CD CD CD CD CD CD CD CD CD CD  
crt_crtreportblocktype.cpp(29) : {54} client block at 0x00314F38, subtype 2, 20 bytes long.  
 Data: <                > CD CD CD CD CD CD CD CD CD CD CD CD CD CD CD CD  
crt_crtreportblocktype.cpp(28) : {53} client block at 0x00314F00, subtype 1, 10 bytes long.  
 Data: <          > CD CD CD CD CD CD CD CD CD CD  
crt_crtreportblocktype.cpp(27) : {52} normal block at 0x00314EC8, 10 bytes long.  
 Data: <          > CD CD CD CD CD CD CD CD CD CD  
Object dump complete.  
```  
  
## See Also  
 [_CrtDoForAllClientObjects](../vs140/_CrtDoForAllClientObjects.md)   
 [_CrtSetDumpClient](../vs140/_CrtSetDumpClient.md)   
 [_CrtMemDumpAllObjectsSince](../vs140/_CrtMemDumpAllObjectsSince.md)   
 [_CrtDumpMemoryLeaks](../vs140/_CrtDumpMemoryLeaks.md)