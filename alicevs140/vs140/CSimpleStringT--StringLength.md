---
title: "CSimpleStringT::StringLength"
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
ms.assetid: d5f17ebe-f4a4-4795-8928-86e94ea0996c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSimpleStringT::StringLength
Returns the number of characters in the specified string.  
  
## Syntax  
  
```  
  
      ATL_NOINLINE static int StringLength(  
   PCXSTR psz  
) throw( );  
```  
  
#### Parameters  
 `psz`  
 A pointer to a null-terminated string.  
  
## Return Value  
 The number of characters in `psz`; not counting a null terminator.  
  
## Remarks  
 Call this method to retrieve the number of characters in the string pointed to by `psz`.  
  
## Example  
 The following example demonstrates the use of `CSimpleStringT::StringLength`.  
  
 [!CODE [NVC_ATLMFC_Utilities#91](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#91)]  
  
## Requirements  
 **Header:** atlsimpstr.h  
  
## See Also  
 [CSimpleStringT Class](../vs140/CSimpleStringT-Class.md)