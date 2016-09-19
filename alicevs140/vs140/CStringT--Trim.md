---
title: "CStringT::Trim"
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
ms.assetid: e7260dc3-5a75-41a4-9c6c-c16681601c62
caps.latest.revision: 18
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStringT::Trim
Trims leading and trailing characters from the string.  
  
## Syntax  
  
```  
CStringT& Trim(  
   XCHAR chTarget   
);  
CStringT& Trim(  
   PCXSTR pszTargets   
);  
CStringT& Trim( );  
```  
  
#### Parameters  
 `chTarget`  
 The target character to be trimmed.  
  
 `pszTargets`  
 A pointer to a string containing the target characters to be trimmed. All leading and trailing occurrences of characters in `pszTarget` will be trimmed from the `CStringT` object.  
  
## Return Value  
 Returns the trimmed string.  
  
## Remarks  
 Removes all leading and trailing occurrences of one of the following:  
  
-   The character specified by `chTarget.`  
  
-   All characters found in the string specified by `pszTargets.`  
  
-   Whitespace.  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#136](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#136)]  
  
## Remarks  
 The output from this example is as follows:  
  
 `Before: "******Soccer is best, but liquor is quicker!?!?!?!?!"`  
  
 `After : "Soccer is best, but liquor is quicker"`  
  
## Requirements  
 **Header:** cstringt.h  
  
## See Also  
 [CStringT Class](../vs140/CStringT-Class.md)   
 [CStringT::TrimLeft](../vs140/CStringT--TrimLeft.md)   
 [CStringT::TrimRight](../vs140/CStringT--TrimRight.md)