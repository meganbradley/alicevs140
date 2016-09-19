---
title: "CStringT::FormatV"
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
ms.assetid: 0330ddca-4fa4-492b-b909-843e5f622ad3
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStringT::FormatV
Formats a message string using a variable argument list.  
  
## Syntax  
  
```  
void FormatV(  
   PCXSTR pszFormat,  
   va_list args  
);  
```  
  
#### Parameters  
 `pszFormat`  
 Points to the format-control string. It will be scanned for inserts and formatted accordingly. The format string is similar to run-time function `printf`-style format strings, except it allows for the parameters to be inserted in an arbitrary order.  
  
 `args`  
 Pointer to a list of arguments.  
  
## Remarks  
 Writes a formatted string and a variable list of arguments to a `CStringT` string in the same way that `vsprintf_s` formats data into a C-style character array.  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#119](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#119)]  
  
 [!CODE [NVC_ATLMFC_Utilities#120](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#120)]  
  
## Requirements  
 **Header:** cstringt.h  
  
## See Also  
 [CStringT Class](../vs140/CStringT-Class.md)