---
title: "Diagnostic Services"
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
ms.assetid: 8d78454f-9fae-49c2-88c9-d3fabd5393e8
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Diagnostic Services
The Microsoft Foundation Class Library supplies many diagnostic services that make debugging your programs easier. These diagnostic services include macros and global functions that allow you to track your program's memory allocations, dump the contents of objects during run time, and print debugging messages during run time. The macros and global functions for diagnostic services are grouped into the following categories:  
  
-   General diagnostic macros  
  
-   General diagnostic functions and variables  
  
-   Object diagnostic functions  
  
 These macros and functions are available for all classes derived from `CObject` in the Debug and Release versions of MFC. However, all except `DEBUG_NEW` and **VERIFY** do nothing in the Release version.  
  
 In the Debug library, all allocated memory blocks are bracketed with a series of "guard bytes." If these bytes are disturbed by an errant memory write, then the diagnostic routines can report a problem. If you include the line:  
  
 [!CODE [NVC_MFCCObjectSample#14](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCObjectSample#14)]  
  
 in your implementation file, all calls to **new** will store the filename and line number where the memory allocation took place. The function [CMemoryState::DumpAllObjectsSince](../vs140/CMemoryState--DumpAllObjectsSince.md) will display this extra information, allowing you to identify memory leaks. Refer also to the class [CDumpContext](../vs140/CDumpContext-Class.md) for additional information on diagnostic output.  
  
 In addition, the C run-time library also supports a set of diagnostic functions you can use to debug your applications. For more information, see [Debug Routines](../vs140/Debug-Routines.md) in the Run-Time Library Reference.  
  
### MFC General Diagnostic Macros  
  
|||  
|-|-|  
|[ASSERT](../vs140/ASSERT--MFC-.md)|Prints a message and then aborts the program if the specified expression evaluates to **FALSE** in the Debug version of the library.|  
|[ASSERT_KINDOF](../vs140/ASSERT_KINDOF.md)|Tests that an object is an object of the specified class or of a class derived from the specified class.|  
|[ASSERT_VALID](../vs140/ASSERT_VALID.md)|Tests the internal validity of an object by calling its `AssertValid` member function; typically overridden from `CObject`.|  
|[DEBUG_NEW](../vs140/DEBUG_NEW.md)|Supplies a filename and line number for all object allocations in Debug mode to help find memory leaks.|  
|[DEBUG_ONLY](../vs140/DEBUG_ONLY.md)|Similar to **ASSERT** but does not test the value of the expression; useful for code that should execute only in Debug mode.|  
|[TRACE](../vs140/TRACE.md)|Provides `printf`-like capability in the Debug version of the library.|  
|[VERIFY](../vs140/VERIFY.md)|Similar to **ASSERT** but evaluates the expression in the Release version of the library as well as in the Debug version.|  
  
### MFC General Diagnostic Variables and Functions  
  
|||  
|-|-|  
|[afxDump](../vs140/afxDump--CDumpContext-in-MFC-.md)|Global variable that sends [CDumpContext](../vs140/CDumpContext-Class.md) information to the debugger output window or to the debug terminal.|  
|[afxMemDF](../vs140/afxMemDF.md)|Global variable that controls the behavior of the debugging memory allocator.|  
|[AfxCheckError](../vs140/AfxCheckError.md)|Global variable used to test the passed **SCODE** to see if it is an error and, if so, throws the appropriate error.|  
|[AfxCheckMemory](../vs140/AfxCheckMemory.md)|Checks the integrity of all currently allocated memory.|  
|[AfxDump](../vs140/AfxDump--MFC-.md)|If called while in the debugger, dumps the state of an object while debugging.|  
|[AfxDumpStack](../vs140/AfxDumpStack.md)|Generate an image of the current stack. This function is always linked statically.|  
|[AfxEnableMemoryLeakDump](../vs140/AfxEnableMemoryLeakDump.md)|Enables the memory leak dump.|  
|[AfxEnableMemoryTracking](../vs140/AfxEnableMemoryTracking.md)|Turns memory tracking on and off.|  
|[AfxIsMemoryBlock](../vs140/AfxIsMemoryBlock.md)|Verifies that a memory block has been properly allocated.|  
|[AfxIsValidAddress](../vs140/AfxIsValidAddress.md)|Verifies that a memory address range is within the program's bounds.|  
|[AfxIsValidString](../vs140/AfxIsValidString.md)|Determines whether a pointer to a string is valid.|  
|[AfxSetAllocHook](../vs140/AfxSetAllocHook.md)|Enables the calling of a function on each memory allocation.|  
  
### MFC Object Diagnostic Functions  
  
|||  
|-|-|  
|[AfxDoForAllClasses](../vs140/AfxDoForAllClasses.md)|Performs a specified function on all `CObject`-derived classes that support run-time type checking.|  
|[AfxDoForAllObjects](../vs140/AfxDoForAllObjects.md)|Performs a specified function on all `CObject`-derived objects that were allocated with **new**.|  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)