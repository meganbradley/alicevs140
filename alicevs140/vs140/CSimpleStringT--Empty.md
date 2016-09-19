---
title: "CSimpleStringT::Empty"
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
ms.assetid: 8e6547f3-7ef5-4def-9052-2d14a8182f7b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSimpleStringT::Empty
Makes this `CSimpleStringT` object an empty string and frees memory as appropriate.  
  
## Syntax  
  
```  
  
void Empty( ) throw( );  
  
```  
  
## Remarks  
 For more information, see [Strings: CString Exception Cleanup](../vs140/CString-Exception-Cleanup.md).  
  
## Example  
 The following example demonstrates the use of `CSimpleStringT::Empty`.  
  
 [!CODE [NVC_ATLMFC_Utilities#78](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#78)]  
  
## Requirements  
 **Header:** atlsimpstr.h  
  
## See Also  
 [CSimpleStringT Class](../vs140/CSimpleStringT-Class.md)   
 [CSimpleStringT::IsEmpty](../vs140/CSimpleStringT--IsEmpty.md)