---
title: "Debugging and Error Reporting Macros"
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
ms.assetid: 4da9b87f-ec5c-4a32-ab93-637780909b9d
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Debugging and Error Reporting Macros
These macros provide useful debugging and trace facilities.  
  
|||  
|-|-|  
|[_ATL_DEBUG_INTERFACES](../vs140/_ATL_DEBUG_INTERFACES.md)|Writes, to the output window, any interface leaks that are detected when `_Module.Term` is called.|  
|[_ATL_DEBUG_QI](../vs140/_ATL_DEBUG_QI.md)|Writes all calls to `QueryInterface` to the output window.|  
|[ATLASSERT](../vs140/ATLASSERT.md)|Performs the same functionality as the [_ASSERTE](../vs140/_ASSERT--_ASSERTE--_ASSERT_EXPR-Macros.md) macro found in the C run-time library.|  
|[ATLENSURE](../vs140/ATLENSURE.md)|Performs parameters validation. Call `AtlThrow` if needed|  
|[ATLTRACENOTIMPL](../vs140/ATLTRACENOTIMPL.md)|Sends a message to the dump device that the specified function is not implemented.|  
|[ATLTRACE](../vs140/ATLTRACE--ATL-.md)|Reports warnings to an output device, such as the debugger window, according to the indicated flags and levels. Included for backward compatibility.|  
|[ATLTRACE2](../vs140/ATLTRACE2.md)|Reports warnings to an output device, such as the debugger window, according to the indicated flags and levels.|  
  
## See Also  
 [Macros](../vs140/ATL-Macros.md)   
 [Debugging and Error Reporting Global Functions](../vs140/Debugging-and-Error-Reporting-Global-Functions.md)