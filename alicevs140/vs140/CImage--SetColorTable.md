---
title: "CImage::SetColorTable"
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
ms.assetid: 5f15dd7f-c979-4b01-a2fd-d1724c03c5b4
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CImage::SetColorTable
Sets the red, green, blue (RGB) color values for a range of entries in the palette of the DIB section.  
  
## Syntax  
  
```  
  
      void SetColorTable(  
   UINT iFirstColor,  
   UINT nColors,  
   const RGBQUAD* prgbColors   
) throw( );  
```  
  
#### Parameters  
 `iFirstColor`  
 The color table index of the first entry to set.  
  
 `nColors`  
 The number of color table entries to set.  
  
 `prgbColors`  
 A pointer to the array of [RGBQUAD](http://msdn.microsoft.com/library/windows/desktop/dd162938) structures to set the color table entries.  
  
## Remarks  
 This method supports only DIB section bitmaps.  
  
## Requirements  
 **Header:** atlimage.h  
  
## See Also  
 [CImage Class](../vs140/CImage-Class.md)   
 [CImage::GetColorTable](../vs140/CImage--GetColorTable.md)