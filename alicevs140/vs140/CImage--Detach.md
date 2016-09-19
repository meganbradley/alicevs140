---
title: "CImage::Detach"
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
ms.assetid: 5cf81c0b-5a27-421d-9b6b-ace3f0e6d25f
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CImage::Detach
Detaches a bitmap from a `CImage` object.  
  
## Syntax  
  
```  
  
HBITMAP Detach( ) throw( );  
  
```  
  
## Return Value  
 A handle to the bitmap detached, or **NULL** if no bitmap is attached.  
  
## Requirements  
 **Header:** atlimage.h  
  
## See Also  
 [CImage Class](../vs140/CImage-Class.md)   
 [CImage::Destroy](../vs140/CImage--Destroy.md)