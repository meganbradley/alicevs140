---
title: "afxMemDF"
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
ms.assetid: cf117501-5446-4fce-81b3-f7194bc95086
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# afxMemDF
This variable is accessible from a debugger or your program and allows you to tune allocation diagnostics.  
  
## Syntax  
  
```  
  
int afxMemDF;  
```  
  
## Remarks  
 `afxMemDF` can have the following values as specified by the enumeration `afxMemDF`:  
  
-   **allocMemDF** Turns on debugging allocator (default setting in Debug library).  
  
-   **delayFreeMemDF** Delays freeing memory. While your program frees a memory block, the allocator does not return that memory to the underlying operating system. This will place maximum memory stress on your program.  
  
-   **checkAlwaysMemDF** Calls `AfxCheckMemory` every time memory is allocated or freed. This will significantly slow memory allocations and deallocations.  
  
## Example  
 [!CODE [NVC_MFC_Utilities#30](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_Utilities#30)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)