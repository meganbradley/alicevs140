---
title: "CImage::SetTransparentColor"
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
ms.assetid: 33f0850e-a3c2-4499-919c-8eb1c074cabc
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CImage::SetTransparentColor
Sets a color at a given indexed location as transparent.  
  
## Syntax  
  
```  
  
      LONG SetTransparentColor(  
   LONG iTransparentColor   
) throw( );  
```  
  
#### Parameters  
 *iTransparentColor*  
 The index, in a color palette, of the color to set to transparent. If –1, no color is set to transparent.  
  
## Return Value  
 The index of the color previously set as transparent.  
  
## Requirements  
 **Header:** atlimage.h  
  
## See Also  
 [CImage Class](../vs140/CImage-Class.md)   
 [CImage::GetTransparentColor](../vs140/CImage--GetTransparentColor.md)