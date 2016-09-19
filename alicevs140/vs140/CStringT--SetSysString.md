---
title: "CStringT::SetSysString"
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
ms.assetid: 283d7a05-4bb4-479b-a1c4-8a0ab08d81d0
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStringT::SetSysString
Reallocates the `BSTR` pointed to by `pbstr` and copies the contents of the `CStringT` object into it, including the `NULL` character.  
  
## Syntax  
  
```  
BSTR SetSysString(  
   BSTR* pbstr  
) const;  
```  
  
#### Parameters  
 `pbstr`  
 A pointer to a character string.  
  
## Return Value  
 The new string.  
  
## Remarks  
 Depending on the contents of the `CStringT` object, the value of the `BSTR` referenced by `pbstr` can change. The function throws a `CMemoryException` if insufficient memory exists.  
  
 This function is normally used to change the value of strings passed by reference for Automation.  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#132](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#132)]  
  
## Requirements  
 **Header:** cstringt.h  
  
## See Also  
 [CStringT Class](../vs140/CStringT-Class.md)   
 [CMemoryException Class](../vs140/CMemoryException-Class.md)