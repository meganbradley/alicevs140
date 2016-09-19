---
title: "CSimpleStringT::Truncate"
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
ms.assetid: 47c8081b-85ea-4042-b890-67b802d8db9f
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSimpleStringT::Truncate
Truncates the string to the new length.  
  
## Syntax  
  
```  
void Truncate(  
   int nNewLength   
);  
```  
  
#### Parameters  
 `nNewLength`  
 The new length of the string.  
  
## Remarks  
 Call this method to truncate the contents of the string to the new length.  
  
> [!NOTE]
>  This does not affect the allocated length of the buffer. To decrease or increase the current buffer, see [FreeExtra](../vs140/CSimpleStringT--FreeExtra.md) and [Preallocate](../vs140/CSimpleStringT--Preallocate.md).  
  
## Example  
 The following example demonstrates the use of `CSimpleStringT::Truncate`.  
  
 [!CODE [NVC_ATLMFC_Utilities#92](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#92)]  
  
## Requirements  
 **Header:** atlsimpstr.h  
  
## See Also  
 [CSimpleStringT Class](../vs140/CSimpleStringT-Class.md)