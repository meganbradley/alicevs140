---
title: "CDC::AlphaBlend"
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
ms.assetid: f6409574-13a2-4126-adfd-84cc124b6c0f
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::AlphaBlend
Call this member function to display bitmaps that have transparent or semitransparent pixels.  
  
## Syntax  
  
```  
  
      BOOL AlphaBlend(  
   int xDest,  
   int yDest,  
   int nDestWidth,  
   int nDestHeight,  
   CDC* pSrcDC,  
   int xSrc,  
   int ySrc,  
   int nSrcWidth,  
   int nSrcHeight,  
   BLENDFUNCTION blend   
);  
```  
  
#### Parameters  
 `xDest`  
 Specifies the x-coordinate, in logical units, of the upper-left corner of the destination rectangle.  
  
 `yDest`  
 Specifies the y-coordinate, in logical units, of the upper-left corner of the destination rectangle.  
  
 `nDestWidth`  
 Specifies the width, in logical units, of the destination rectangle.  
  
 `nDestHeight`  
 Specifies the height, in logical units, of the destination rectangle.  
  
 `pSrcDC`  
 A pointer to the source device context.  
  
 `xSrc`  
 Specifies the x-coordinate, in logical units, of the upper-left corner of the source rectangle.  
  
 `ySrc`  
 Specifies the y-coordinate, in logical units, of the upper-left corner of the source rectangle.  
  
 `nSrcWidth`  
 Specifies the width, in logical units, of the source rectangle.  
  
 `nSrcHeight`  
 Specifies the height, in logical units, of the source rectangle.  
  
 *blend*  
 Specifies a [BLENDFUNCTION](http://msdn.microsoft.com/library/windows/desktop/dd183393) structure.  
  
## Return Value  
 **TRUE** if successful; otherwise **FALSE**.  
  
## Remarks  
 See [AlphaBlend](http://msdn.microsoft.com/library/windows/desktop/dd183351) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)] for more information.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [EMRALPHABLEND](http://msdn.microsoft.com/library/windows/desktop/dd162513)