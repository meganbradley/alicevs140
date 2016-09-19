---
title: "CW2CWEX::CW2CWEX"
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
ms.assetid: a1a633b2-7d28-4c52-a44d-93fab79b2127
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CW2CWEX::CW2CWEX
The constructor.  
  
## Syntax  
  
```  
  
      CW2CWEX(  
   LPCWSTR psz,  
   UINT nCodePage  
) throw(...);  
CW2CWEX(  
   LPCWSTR psz  
) throw(...);  
```  
  
#### Parameters  
 `psz`  
 The text string to be converted.  
  
 `nCodePage`  
 The code page. Not used in this class.  
  
## Remarks  
 Allocates the buffer used in the translation process.  
  
## Requirements  
 **Header:** atlconv.h  
  
## See Also  
 [CW2CWEX Class](../vs140/CW2CWEX-Class.md)