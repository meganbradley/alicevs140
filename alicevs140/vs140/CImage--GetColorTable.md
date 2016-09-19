---
title: "CImage::GetColorTable"
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
ms.assetid: f0a9d745-fc68-48ef-81e9-1a6b2d7542f4
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CImage::GetColorTable
Retrieves red, green, blue (RGB) color values from a range of entries in the palette of the DIB section.  
  
## Syntax  
  
```  
  
      void GetColorTable(  
   UINT iFirstColor,  
   UINT nColors,  
   RGBQUAD* prgbColors   
) const throw( );  
```  
  
#### Parameters  
 `iFirstColor`  
 The color table index of the first entry to retrieve.  
  
 `nColors`  
 The number of color table entries to retrieve.  
  
 `prgbColors`  
 A pointer to the array of [RGBQUAD](http://msdn.microsoft.com/library/windows/desktop/dd162938) structures to retrieve the color table entries.  
  
## Requirements  
 **Header:** atlimage.h  
  
## See Also  
 [CImage Class](../vs140/CImage-Class.md)   
 [CImage::SetColorTable](../vs140/CImage--SetColorTable.md)   
 [CImage::GetMaxColorTableEntries](../vs140/CImage--GetMaxColorTableEntries.md)   
 [GetDIBColorTable](http://msdn.microsoft.com/library/windows/desktop/dd144878)