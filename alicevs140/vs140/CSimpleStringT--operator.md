---
title: "CSimpleStringT::operator"
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
ms.assetid: 88c1c714-f56e-4ab4-bb5f-41bc7921ccbc
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSimpleStringT::operator
Call this function to access a single character of the character array.  
  
## Syntax  
  
```  
  
      XCHAR operator[](int iChar) const;  
```  
  
#### Parameters  
 `iChar`  
 Zero-based index of a character in the string.  
  
## Remarks  
 The overloaded subscript (`[]`) operator returns a single character specified by the zero-based index in `iChar`. This operator is a convenient substitute for the [GetAt](../vs140/CSimpleStringT--GetAt.md) member function.  
  
> [!NOTE]
>  You can use the subscript (`[]`) operator to get the value of a character in a `CSimpleStringT`, but you cannot use it to change the value of a character in a `CSimpleStringT`.  
  
## Example  
 The following example demonstrates the use of **CSimpleStringT::operator []**.  
  
 [!CODE [NVC_ATLMFC_Utilities#95](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#95)]  
  
## Requirements  
 **Header:** atlsimpstr.h  
  
## See Also  
 [CSimpleStringT Class](../vs140/CSimpleStringT-Class.md)   
 [CSimpleStringT::SetAt](../vs140/CSimpleStringT--SetAt.md)