---
title: "CBitmapRenderTarget::GetBitmap"
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
ms.assetid: c96997b4-8012-490a-8897-4007c546690a
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBitmapRenderTarget::GetBitmap
Retrieves the bitmap for this render target. The returned bitmap can be used for drawing operations.  
  
## Syntax  
  
```  
BOOL GetBitmap(  
   CD2DBitmap& bitmap  
);  
```  
  
#### Parameters  
 `bitmap`  
 When this method returns, contains the valid bitmap for this render target. This bitmap can be used for drawing operations.  
  
## Return Value  
 If the method succeeds, it returns TRUE. Otherwise, it returns FALSE.  
  
## Requirements  
 **Header:** afxrendertarget.h  
  
## See Also  
 [CBitmapRenderTarget Class](../vs140/CBitmapRenderTarget-Class.md)