---
title: "CBitmap::CreateBitmapIndirect"
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
ms.assetid: a50ed794-c700-45b3-ba9f-cae03a402515
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBitmap::CreateBitmapIndirect
Initializes a bitmap that has the width, height, and bit pattern (if one is specified) given in the structure pointed to by `lpBitmap`.  
  
## Syntax  
  
```  
  
      BOOL CreateBitmapIndirect(  
   LPBITMAP lpBitmap   
);  
```  
  
#### Parameters  
 `lpBitmap`  
 Points to a [BITMAP](../vs140/BITMAP-Structure.md) structure that contains information about the bitmap.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 Although a bitmap cannot be directly selected for a display device, it can be selected as the current bitmap for a memory device context by using [CDC::SelectObject](../vs140/CDC--SelectObject.md) and copied to any compatible device context by using the [CDC::BitBlt](../vs140/CDC--BitBlt.md) or [CDC::StretchBlt](../vs140/CDC--StretchBlt.md) function. (The [CDC::PatBlt](../vs140/CDC--PatBlt.md) function can copy the bitmap for the current brush directly to the display device context.)  
  
 If the **BITMAP** structure pointed to by the `lpBitmap` parameter has been filled in by using the `GetObject` function, the bits of the bitmap are not specified and the bitmap is uninitialized. To initialize the bitmap, an application can use a function such as [CDC::BitBlt](../vs140/CDC--BitBlt.md) or [SetDIBits](http://msdn.microsoft.com/library/windows/desktop/dd162973) to copy the bits from the bitmap identified by the first parameter of `CGdiObject::GetObject` to the bitmap created by `CreateBitmapIndirect`.  
  
 When you finish with the `CBitmap` object created with `CreateBitmapIndirect` function, first select the bitmap out of the device context, then delete the `CBitmap` object.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CBitmap Class](../vs140/CBitmap-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::SelectObject](../vs140/CDC--SelectObject.md)   
 [CDC::BitBlt](../vs140/CDC--BitBlt.md)   
 [CGdiObject::DeleteObject](../vs140/CGdiObject--DeleteObject.md)   
 [CGdiObject::GetObject](../vs140/CGdiObject--GetObject.md)   
 [CreateBitmapIndirect](http://msdn.microsoft.com/library/windows/desktop/dd183486)