---
title: "CImage::IsTransparencySupported"
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
ms.assetid: cedad957-a3b9-4822-828c-a76b7717e0ac
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CImage::IsTransparencySupported
Indicates whether the application supports transparent bitmaps and was compiled for Windows 2000 or later.  
  
## Syntax  
  
```  
  
static BOOL IsTransparencySupported( ) throw( );  
  
```  
  
## Return Value  
 Nonzero if the current platform supports transparency. Otherwise 0.  
  
## Remarks  
 If the return value is nonzero, and transparency is supported, a call to [AlphaBlend](../vs140/CImage--AlphaBlend.md), [TransparentBlt](../vs140/CImage--TransparentBlt.md), or [Draw](../vs140/CImage--Draw.md) will handle transparent colors.  
  
 If the application is compiled for use with operating systems before Windows 2000 or Windows 98, this method will always return 0, even on newer operating systems.  
  
 See [CImage Limitations with Earlier Operating Systems](../vs140/CImage-Limitations-with-Earlier-Operating-Systems.md) for more detailed information.  
  
## Requirements  
 **Header:** atlimage.h  
  
## See Also  
 [CImage Class](../vs140/CImage-Class.md)   
 [CImage::GetTransparentColor](../vs140/CImage--GetTransparentColor.md)