---
title: "CDefaultCharTraits::CharToLower"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: acefb705-b134-46b0-862e-c35ad31e59c7
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDefaultCharTraits::CharToLower
Call this function to convert a character to lowercase.  
  
## Syntax  
  
```  
  
      static wchar_t CharToLower(  
   wchar_t x  
);  
static char CharToLower(  
   char x  
);  
```  
  
#### Parameters  
 *x*  
 The character to convert to lowercase.  
  
## Example  
 [!CODE [NVC_ATL_Utilities#132](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#132)]  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CDefaultCharTraits::CharToUpper](../vs140/CDefaultCharTraits--CharToUpper.md)