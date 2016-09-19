---
title: "CBitmap::SetBitmapBits"
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
ms.assetid: 36b3b068-09f4-45d9-8eea-6c3757dcc74d
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBitmap::SetBitmapBits
Sets the bits of a bitmap to the bit values given by `lpBits`.  
  
## Syntax  
  
```  
  
      DWORD SetBitmapBits(  
   DWORD dwCount,  
   const void* lpBits   
);  
```  
  
#### Parameters  
 `dwCount`  
 Specifies the number of bytes pointed to by `lpBits`.  
  
 `lpBits`  
 Points to the **BYTE** array that contains the pixel values to be copied to the `CBitmap` object. In order for the bitmap to be able to render its image correctly, the values should be formatted to conform to the height, width and color depth values that were specified when the CBitmap instance was created. For more information, see [CBitmap::CreateBitmap](../vs140/CBitmap--CreateBitmap.md).  
  
## Return Value  
 The number of bytes used in setting the bitmap bits; 0 if the function fails.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CBitmap Class](../vs140/CBitmap-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [SetBitmapBits](http://msdn.microsoft.com/library/windows/desktop/dd162962)