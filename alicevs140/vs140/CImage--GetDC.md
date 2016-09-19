---
title: "CImage::GetDC"
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
ms.assetid: 4cbb0bc9-4545-402e-b0cd-9058097a7d1b
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CImage::GetDC
Retrieves the device context that currently has the image selected into it.  
  
## Syntax  
  
```  
  
HDC GetDC( ) const throw( );  
  
```  
  
## Return Value  
 A handle to a device context.  
  
## Remarks  
 For each call to `GetDC`, you must have a subsequent call to [ReleaseDC](../vs140/CImage--ReleaseDC.md).  
  
## Requirements  
 **Header:** atlimage.h  
  
## See Also  
 [CImage Class](../vs140/CImage-Class.md)   
 [CImage::GetBits](../vs140/CImage--GetBits.md)   
 [CImage::GetBPP](../vs140/CImage--GetBPP.md)