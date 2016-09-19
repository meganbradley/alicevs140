---
title: "CStringT::GetEnvironmentVariable"
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
ms.assetid: 614669e6-01ce-4dc8-afdb-4a49fc393451
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStringT::GetEnvironmentVariable
Sets the string to the value of the specified environment variable.  
  
## Syntax  
  
```  
BOOL GetEnvironmentVariable(  
   PCXSTR pszVar  
);  
```  
  
#### Parameters  
 `pszVar`  
 Pointer to a null-terminated string that specifies the environment variable.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 Retrieves the value of the specified variable from the environment block of the calling process. The value is in the form of a null-terminated string of characters.  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#121](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#121)]  
  
## Requirements  
 **Header:** cstringt.h  
  
## See Also  
 [CStringT Class](../vs140/CStringT-Class.md)