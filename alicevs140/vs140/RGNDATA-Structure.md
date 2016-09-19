---
title: "RGNDATA Structure"
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
ms.topic: article
ms.assetid: 72257c00-f440-4dca-979e-9b6b5b2d5f2f
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# RGNDATA Structure
The `RGNDATA` structure contains a header and an array of rectangles that compose a region. These rectangles, sorted top to bottom left to right, do not overlap.  
  
## Syntax  
  
```  
  
      typedef struct _RGNDATA { /* rgnd */  
   RGNDATAHEADER rdh;  
   char Buffer[1];  
} RGNDATA;  
```  
  
#### Parameters  
 *rdh*  
 Specifies a [RGNDATAHEADER](http://msdn.microsoft.com/library/windows/desktop/dd162941) structure. (For more information on this structure, see the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].) The members of this structure specify the type of region (whether it is rectangular or trapezoidal), the number of rectangles that make up the region, the size of the buffer that contains the rectangle structures, and so on.  
  
 `Buffer`  
 Specifies an arbitrary-size buffer that contains the [RECT](../vs140/RECT-Structure.md) structures that make up the region.  
  
## Requirements  
 **Header:** wingdi.h  
  
## See Also  
 [Structures, Styles, Callbacks, and Message Maps](../vs140/Structures--Styles--Callbacks--and-Message-Maps.md)   
 [CRgn::CreateFromData](../vs140/CRgn--CreateFromData.md)   
 [CRgn::GetRegionData](../vs140/CRgn--GetRegionData.md)