---
title: "CStringT::AnsiToOem"
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
ms.assetid: d6c3e893-7cdc-469d-ae40-e8c8c257da95
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStringT::AnsiToOem
Converts all the characters in this `CStringT` object from the ANSI character set to the OEM character set.  
  
## Syntax  
  
```  
void AnsiToOem();  
```  
  
## Remarks  
 The function is not available if `_UNICODE` is defined.  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#106](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#106)]  
  
## Requirements  
 **Header:** cstringt.h  
  
## See Also  
 [CStringT Class](../vs140/CStringT-Class.md)