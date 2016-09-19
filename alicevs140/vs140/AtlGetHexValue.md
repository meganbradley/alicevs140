---
title: "AtlGetHexValue"
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
ms.assetid: d6868900-7e1b-44c0-9a73-9635f3f2811e
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AtlGetHexValue
Call this function to get the numeric value of a hexadecimal digit.  
  
## Syntax  
  
```  
  
      inline char AtlGetHexValue(  
   char chIn   
) throw( );  
```  
  
#### Parameters  
 `chIn`  
 The hexadecimal character '0'-'9', 'A'-'F', or 'a'-'f'.  
  
## Return Value  
 The numeric value of the input character interpreted as a hexadecimal digit. For example, an input of '0' returns a value of 0 and an input of 'A' returns a value of 10. If the input character is not a hexadecimal digit, this function returns -1.  
  
## Requirements  
 **Header:** atlenc.h  
  
## See Also  
 [ATL Concepts](../vs140/Active-Template-Library--ATL--Concepts.md)   
 [ATL Reference](../vs140/ATL-COM-Desktop-Components.md)   
 [ATL Functions Alphabetical Reference](../vs140/ATL-Functions-Alphabetical-Reference.md)