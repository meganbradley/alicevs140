---
title: "CSimpleStringT::SetAt"
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
ms.assetid: 66deb157-2b73-40f8-a2f6-8c92534bb126
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSimpleStringT::SetAt
Sets a single character from a `CSimpleStringT` object.  
  
## Syntax  
  
```  
  
      void SetAt(  
   int iChar,  
   XCHAR ch  
);  
```  
  
#### Parameters  
 `iChar`  
 Zero-based index of the character in the `CSimpleStringT` object. The `iChar` parameter must be greater than or equal to 0 and less than the value returned by [GetLength](../vs140/CSimpleStringT--GetLength.md).  
  
 *ch*  
 The new character.  
  
## Remarks  
 Call this method to overwrite the character located at `iChar`. This method will not enlarge the string if `iChar` exceeds the bounds of the existing string.  
  
## Example  
 The following example demonstrates the use of `CSimpleStringT::SetAt`.  
  
 [!CODE [NVC_ATLMFC_Utilities#88](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#88)]  
  
## Requirements  
 **Header:** atlsimpstr.h  
  
## See Also  
 [CSimpleStringT Class](../vs140/CSimpleStringT-Class.md)   
 [CSimpleStringT::GetAt](../vs140/CSimpleStringT--GetAt.md)   
 [CSimpleStringT::operator](../vs140/CSimpleStringT--operator.md)