---
title: "CSimpleStringT::FreeExtra"
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
ms.assetid: 448e8bb3-be9c-488f-aab0-443d87e7d126
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSimpleStringT::FreeExtra
Frees any extra memory previously allocated by the string but no longer needed.  
  
## Syntax  
  
```  
void FreeExtra( );  
```  
  
## Remarks  
 This should reduce the memory overhead consumed by the string object. The method reallocates the buffer to the exact length returned by [GetLength](../vs140/CSimpleStringT--GetLength.md).  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#79](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#79)]  
  
## Remarks  
 The output from this example is as follows:  
  
 `Alloc length is 1031, String length is 1024`  
  
 `Alloc length is 1031, String length is 15`  
  
 `Alloc length is 15, String length is 15`  
  
## Requirements  
 **Header:** atlsimpstr.h  
  
## See Also  
 [CSimpleStringT Class](../vs140/CSimpleStringT-Class.md)