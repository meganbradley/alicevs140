---
title: "CSimpleStringT::GetString"
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
ms.assetid: 6674050e-2188-44ab-8408-5df8a4e1c27c
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSimpleStringT::GetString
Retrieves the character string.  
  
## Syntax  
  
```  
PCXSTR GetString( ) const throw( );  
```  
  
## Return Value  
 A pointer to a null-terminated character string.  
  
## Remarks  
 Call this method to retrieve the character string associated with the `CSimpleStringT` object.  
  
> [!NOTE]
>  The returned `PCXSTR` pointer is `const` and does not allow direct modification of `CSimpleStringT` contents.  
  
## Example  
 The following example demonstrates the use of `CSimpleStringT::GetString`.  
  
 [!CODE [NVC_ATLMFC_Utilities#83](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#83)]  
  
## Requirements  
 **Header:** atlsimpstr.h  
  
## See Also  
 [CSimpleStringT Class](../vs140/CSimpleStringT-Class.md)   
 [CSimpleStringT::GetBuffer](../vs140/CSimpleStringT--GetBuffer.md)