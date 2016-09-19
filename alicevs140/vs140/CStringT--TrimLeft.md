---
title: "CStringT::TrimLeft"
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
ms.assetid: e9a2eb1d-49a4-4e6d-b2b1-297719c65086
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStringT::TrimLeft
Trims leading characters from the string.  
  
## Syntax  
  
```  
CStringT& TrimLeft(  
   XCHAR chTarget   
);  
CStringT& TrimLeft(  
   PCXSTR pszTargets   
);  
CStringT& TrimLeft( );  
```  
  
#### Parameters  
 `chTarget`  
 The target character to be trimmed.  
  
 `pszTargets`  
 A pointer to a string containing the target characters to be trimmed. All leading occurrences of characters in `pszTarget` will be trimmed from the `CStringT` object.  
  
## Return Value  
 The resulting trimmed string.  
  
## Remarks  
 Removes all leading and trailing occurrences of one of the following:  
  
-   The character specified by `chTarget.`  
  
-   All characters found in the string specified by `pszTargets.`  
  
-   Whitespace.  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#137](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#137)]  
  
## Requirements  
 **Header:** cstringt.h  
  
## See Also  
 [CStringT Class](../vs140/CStringT-Class.md)   
 [CStringT::Trim](../vs140/CStringT--Trim.md)   
 [CStringT::TrimRight](../vs140/CStringT--TrimRight.md)