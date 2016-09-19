---
title: "CD2DTextLayout::GetFontFamilyName"
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
ms.assetid: d75ffa01-a4fa-4563-8153-4775c28a35d4
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CD2DTextLayout::GetFontFamilyName
Copies the font family name of the text at the specified position.  
  
## Syntax  
  
```  
CString GetFontFamilyName(  
   UINT32 currentPosition,  
   DWRITE_TEXT_RANGE* textRange = NULL  
) const;  
```  
  
#### Parameters  
 `currentPosition`  
 The position of the text to examine.  
  
 `textRange`  
 The range of text that has the same formatting as the text at the position specified by currentPosition. This means the run has the exact formatting as the position specified, including but not limited to the font family name.  
  
## Return Value  
 CString object that contains the current font family name.  
  
## Requirements  
 **Header:** afxrendertarget.h  
  
## See Also  
 [CD2DTextLayout Class](../vs140/CD2DTextLayout-Class.md)