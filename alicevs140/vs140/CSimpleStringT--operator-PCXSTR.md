---
title: "CSimpleStringT::operator PCXSTR"
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
ms.assetid: cf296f31-8076-49ae-b305-0d1e22488886
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSimpleStringT::operator PCXSTR
Directly accesses characters stored in a `CSimpleStringT` object as a C-style string.  
  
## Syntax  
  
```  
  
operator PCXSTR( ) const throw( );  
  
```  
  
## Return Value  
 A character pointer to the string's data.  
  
## Remarks  
 No characters are copied; only a pointer is returned. Be careful with this operator. If you change a `CString` object after you have obtained the character pointer, you may cause a reallocation of memory that invalidates the pointer.  
  
## Example  
 The following example demonstrates the use of **CSimpleStringT::operator PCXSTR**.  
  
 [!CODE [NVC_ATLMFC_Utilities#96](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#96)]  
  
## Requirements  
 **Header:** atlsimpstr.h  
  
## See Also  
 [CSimpleStringT Class](../vs140/CSimpleStringT-Class.md)