---
title: "RGBToHtml"
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
ms.assetid: 356bb9ca-3b14-4382-b83d-543acdb128f6
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# RGBToHtml
Converts a [COLORREF](http://msdn.microsoft.com/library/windows/desktop/dd183449) value to the HTML text corresponding to that color value.  
  
## Syntax  
  
```  
  
      bool inline RGBToHtml(  
   COLORREF color,  
   LPTSTR pbOut,  
   long nBuffer   
);  
```  
  
#### Parameters  
 `color`  
 An RGB color value.  
  
 `pbOut`  
 Caller-allocated buffer to receive the text for the HTML color value. The buffer must have space for at least 8 characters including space for the null terminator).  
  
 *nBuffer*  
 The size in bytes of the buffer (including space for the null terminator).  
  
## Return Value  
 Returns **TRUE** on success, **FALSE** on failure.  
  
## Remarks  
 An HTML color value is a pound sign followed by a 6-digit hexadecimal value using 2 digits for each of the red, green, and blue components of the color (for example, #FFFFFF is white).  
  
## Requirements  
 **Header:** atlutil.h  
  
## See Also  
 [ATL Concepts](../vs140/Active-Template-Library--ATL--Concepts.md)   
 [ATL Reference](../vs140/ATL-COM-Desktop-Components.md)   
 [ATL Functions Alphabetical Reference](../vs140/ATL-Functions-Alphabetical-Reference.md)