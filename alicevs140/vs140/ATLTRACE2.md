---
title: "ATLTRACE2"
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
ms.assetid: 467ff555-e7a5-4f94-bdd9-50ee27ab9986
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ATLTRACE2
Reports warnings to an output device, such as the debugger window, according to the indicated flags and levels.  
  
## Syntax  
  
```  
  
      ATLTRACE2(   
      exp   
      );  
ATLTRACE2(  
   DWORD category,  
   UINT level,  
   LPCSTR lpszFormat,  
   ...  
);  
```  
  
#### Parameters  
 `exp`  
 [in] The string to send to the Visual C++ output window or any application that traps these messages.  
  
 `category`  
 [in] Type of event or method on which to report. See the Remarks for a list of categories.  
  
 `level`  
 [in] The level of tracing to report. See the Remarks for details.  
  
 `lpszFormat`  
 [in] The `printf`-style format string to use to create a string to send to the dump device.  
  
## Remarks  
 The short form of `ATLTRACE2` writes a string to the debugger's output window. The second form of `ATLTRACE2` also writes output to the debugger's output window, but is subject to the settings of the ATL/MFC Trace Tool (see [ATLTraceTool Sample](../vs140/Visual-C---Samples.md)). For example, if you set `level` to 4 and the ATL/MFC Trace Tool to level 0, you will not see the message. *level* can be 0, 1, 2, 3, or 4. The default, 0, reports only the most serious problems.  
  
 The `category` parameter lists the trace flags to set. These flags correspond to the types of methods for which you want to report. The tables below list the valid trace flags you can use for the `category` parameter.  
  
### ATL Trace Flags  
  
|ATL Category|Description|  
|------------------|-----------------|  
|`atlTraceGeneral`|Reports on all ATL applications. The default.|  
|`atlTraceCOM`|Reports on COM methods.|  
|`atlTraceQI`|Reports on QueryInterface calls.|  
|`atlTraceRegistrar`|Reports on the registration of objects.|  
|`atlTraceRefcount`|Reports on changing reference count.|  
|`atlTraceWindowing`|Reports on windows methods; for example, reports an invalid message map ID.|  
|`atlTraceControls`|Reports on controls; for example, reports when a control or its window is destroyed.|  
|`atlTraceHosting`|Reports hosting messages; for example, reports when a client in a container is activated.|  
|`atlTraceDBClient`|Reports on OLE DB Consumer Template; for example, when a call to GetData fails, the output can contain the HRESULT.|  
|`atlTraceDBProvider`|Reports on OLE DB Provider Template; for example, reports if the creation of a column failed.|  
|`atlTraceSnapin`|Reports for MMC SnapIn application.|  
|`atlTraceNotImpl`|Reports that the indicated function is not implemented.|  
|**atlTraceAllocation**|Reports messages printed by the memory debugging tools in atldbgmem.h.|  
  
### MFC Trace Flags  
  
|MFC Category|Description|  
|------------------|-----------------|  
|**traceAppMsg**|General purpose, MFC messages. Always recommended.|  
|**traceDumpContext**|Messages from [CDumpContext](../vs140/CDumpContext-Class.md).|  
|**traceWinMsg**|Messages from MFC's message handling code.|  
|**traceMemory**|Messages from MFC's memory management code.|  
|**traceCmdRouting**|Messages from MFC's Windows command routing code.|  
|**traceHtml**|Messages from MFC's DHTML dialog support.|  
|**traceSocket**|Messages from MFC's socket support.|  
|**traceOle**|Messages from MFC's OLE support.|  
|**traceDatabase**|Messages from MFC's database support.|  
|**traceInternet**|Messages from MFC's Internet support.|  
  
 To declare a custom trace category, declare a global instance of the `CTraceCategory` class as follows:  
  
 [!CODE [NVC_ATL_Utilities#109](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#109)]  
  
 The category name, `MY_CATEGORY` in this example, is the name you specify to the `category` parameter. The first parameter is the category name that will appear in the ATL/MFC Trace Tool. The second parameter is the default trace level. This parameter is optional, and the default trace level is 0.  
  
 To use a user-defined category:  
  
 [!CODE [NVC_ATL_Utilities#110](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#110)]  
  
 To specify that you want to filter the trace messages, insert definitions for these macros into Stdafx.h before the `#include <atlbase.h>` statement.  
  
 Alternatively, you can set the filter in the preprocessor directives in the **Property Pages** dialog box. Click the **Preprocessor** tab and then insert the global into the **Preprocessor Definitions** edit box.  
  
 Atlbase.h contains default definitions of the `ATLTRACE2` macros and these definitions will be used if you don't define these symbols before atlbase.h is processed.  
  
 In release builds, `ATLTRACE2` compiles to `(void) 0`.  
  
 `ATLTRACE2` limits the contents of the string to be sent to the dump device to no more than 1023 characters, after formatting.  
  
 **ATLTRACE** and `ATLTRACE2` have the same behavior, **ATLTRACE** is included for backward compatibility.  
  
## Example  
 [!CODE [NVC_ATL_Utilities#111](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#111)]  
  
## Requirements  
 **Header:** atltrace.h  
  
## See Also  
 [Debugging and Error Reporting Macros](../vs140/Debugging-and-Error-Reporting-Macros.md)   
 [ATLTRACE](../vs140/ATLTRACE--ATL-.md)