---
title: "_execute_onexit_table, _initialize_onexit_table, _register_onexit_function"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apiname: 
  - _execute_onexit_table
  - _initialize_onexit_table
  - _register_onexit_function
apilocation: 
  - api-ms-win-crt-runtime-l1-1-0.dll
apitype: DLLExport
ms.assetid: ad9e4149-d4ad-4fdf-aaaf-cf786fcb4473
caps.latest.revision: 5
---
# _execute_onexit_table, _initialize_onexit_table, _register_onexit_function
Manages the routines to be called at exit time.  
  
## Syntax  
  
```  
int _initialize_onexit_table(  
    _onexit_table_t* table  
    );  
  
int _register_onexit_function(  
    _onexit_table_t* table,  
    _onexit_t        function  
    );  
  
int _execute_onexit_table(  
    _onexit_table_t* table  
    );  
```  
  
#### Parameters  
 [inout] `table`  
 Pointer to the onexit function table.  
  
 [in] `function`  
 Pointer to a function to add to the onexit function table.  
  
## Return Value  
 If successful, returns 0. Otherwise, returns a negative value.  
  
## Remarks  
 These functions are infrastructure implementation details used to support the C runtime, and should not be called directly from your code. The C runtime uses an *onexit function table* to represent the sequence of functions registered by calls to `atexit`, `at_quick_exit`, and `_onexit`. The onexit function table data structure is an opaque implementation detail of the C runtime; the order and meaning of its data members may change. They should not be inspected by external code.  
  
 The `_initialize_onexit_table` function initializes the onexit function table to its initial value.  This function must be called before the onexit function table is passed to either `_register_onexit_function` or `_execute_onexit_table`.  
  
 The `_register_onexit_function` function appends a function to the end of the onexit function table.  
  
 The `_execute_onexit_table` function executes all of the functions in the onexit function table, clears the table, and then returns. After a call to `_execute_onexit_table`, the table is in a non-valid state; it must be reinitialized by a call to `_initialize_onexit_table` before it is used again.  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_initialize_onexit_table function`, `_register_onexit_function`, `_execute_onexit_table`|C, C++: <process.h>|  
  
 The `_initialize_onexit_table`, `_register_onexit_function`, and `_execute_onexit_table` functions are Microsoft specific. For compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## See Also  
 [atexit](../vs140/atexit.md)   
 [exit, _Exit, _exit](../vs140/exit--_Exit--_exit.md)   
 [_onexit, _onexit_m](../vs140/_onexit--_onexit_m.md)