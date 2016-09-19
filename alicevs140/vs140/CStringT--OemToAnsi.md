---
title: "CStringT::OemToAnsi"
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
ms.assetid: 929d31a9-b9cf-4629-a9a5-c26ac674afe1
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStringT::OemToAnsi
Converts all the characters in this `CStringT` object from the OEM character set to the ANSI character set.  
  
## Syntax  
  
```  
void OemToAnsi();  
```  
  
## Remarks  
 This function is not available if `_UNICODE` is defined.  
  
## Example  
 See the example for [CStringT::AnsiToOem](../vs140/CStringT--AnsiToOem.md).  
  
## Requirements  
 **Header:** cstringt.h  
  
## See Also  
 [CStringT Class](../vs140/CStringT-Class.md)