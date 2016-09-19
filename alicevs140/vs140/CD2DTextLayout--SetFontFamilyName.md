---
title: "CD2DTextLayout::SetFontFamilyName"
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
ms.assetid: c52b6b2b-044a-4c2c-8b7a-0927bc31b0fc
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CD2DTextLayout::SetFontFamilyName
Sets null-terminated font family name for text within a specified text range  
  
## Syntax  
  
```  
BOOL SetFontFamilyName(  
   LPCWSTR pwzFontFamilyName,  
   DWRITE_TEXT_RANGE textRange  
);  
```  
  
#### Parameters  
 `pwzFontFamilyName`  
 The font family name that applies to the entire text string within the range specified by textRange  
  
 `textRange`  
 Text range to which this change applies  
  
## Return Value  
 If the method succeeds, it returns TRUE. Otherwise, it returns FALSE  
  
## Requirements  
 **Header:** afxrendertarget.h  
  
## See Also  
 [CD2DTextLayout Class](../vs140/CD2DTextLayout-Class.md)