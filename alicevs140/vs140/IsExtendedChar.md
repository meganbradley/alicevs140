---
title: "IsExtendedChar"
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
ms.assetid: 9c6721f5-ddfb-478b-a976-fe015bdf2ec1
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IsExtendedChar
Call this function to find out if a given character is an extended character (less than 32, greater than 126, and not a tab, linefeed or carriage return)  
  
## Syntax  
  
```  
  
      inline int IsExtendedChar(  
   char ch   
) throw( );  
```  
  
#### Parameters  
 *ch*  
 The character to be tested  
  
## Return Value  
 **TRUE** if the character is extended, **FALSE** otherwise.  
  
## Requirements  
 **Header:** atlenc.h  
  
## See Also  
 [ATL Concepts](../vs140/Active-Template-Library--ATL--Concepts.md)   
 [ATL Reference](../vs140/ATL-COM-Desktop-Components.md)   
 [ATL Functions Alphabetical Reference](../vs140/ATL-Functions-Alphabetical-Reference.md)