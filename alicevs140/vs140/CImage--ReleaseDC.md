---
title: "CImage::ReleaseDC"
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
ms.assetid: 58ce99a6-f514-4f2d-a762-6d506aa37b33
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CImage::ReleaseDC
Releases the device context.  
  
## Syntax  
  
```  
  
void ReleaseDC( ) const throw( );  
  
```  
  
## Remarks  
 Because only one bitmap can be selected into a device context at a time, you must call `ReleaseDC` for each call to [GetDC](../vs140/CImage--GetDC.md).  
  
## Requirements  
 **Header:** atlimage.h  
  
## See Also  
 [CImage Class](../vs140/CImage-Class.md)