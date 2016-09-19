---
title: "CSimpleStringT::GetAt"
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
ms.assetid: 528beb4b-c115-487a-bac5-e51621d55eb6
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSimpleStringT::GetAt
Returns one character from a `CSimpleStringT` object.  
  
## Syntax  
  
```  
  
      XCHAR GetAt(  
   int iChar  
) const;  
```  
  
#### Parameters  
 `iChar`  
 Zero-based index of the character in the `CSimpleStringT` object. The `iChar` parameter must be greater than or equal to 0 and less than the value returned by [GetLength](../vs140/CSimpleStringT--GetLength.md). Otherwise, `GetAt` will generate an exception.  
  
## Return Value  
 An `XCHAR` that contains the character at the specified position in the string.  
  
## Remarks  
 Call this method to return the one character specified by `iChar`. The overloaded subscript (`[]`) operator is a convenient alias for `GetAt`. The null terminator is addressable without generating an exception by using `GetAt`. However, it is not counted by `GetLength`, and the value returned is 0.  
  
## Example  
 The following example demonstrates how to use `CSimpleStringT::GetAt`.  
  
 [!CODE [NVC_ATLMFC_Utilities#80](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#80)]  
  
## Requirements  
 **Header:** atlsimpstr.h  
  
## See Also  
 [CSimpleStringT Class](../vs140/CSimpleStringT-Class.md)   
 [CSimpleStringT::GetLength](../vs140/CSimpleStringT--GetLength.md)   
 [CSimpleStringT::operator](../vs140/CSimpleStringT--operator.md)