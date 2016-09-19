---
title: "CW2WEX::CW2WEX"
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
ms.assetid: ac57edd7-ec84-46c3-94ba-5a8a3c3143a6
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CW2WEX::CW2WEX
The constructor.  
  
## Syntax  
  
```  
  
      CW2WEX(  
   LPCWSTR psz,  
   UINT nCodePage  
) throw(...);  
CW2WEX(  
   LPCWSTR psz  
 ) throw(...);  
```  
  
#### Parameters  
 `psz`  
 The text string to be converted.  
  
 `nCodePage`  
 The code page. Not used in this class.  
  
## Remarks  
 Creates the buffer required for the translation.  
  
## Requirements  
 **Header:** atlconv.h  
  
## See Also  
 [CW2WEX Class](../vs140/CW2WEX-Class.md)