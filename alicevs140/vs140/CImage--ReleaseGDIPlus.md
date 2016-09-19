---
title: "CImage::ReleaseGDIPlus"
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
ms.assetid: 0d08175f-f853-40f0-a1a9-9bbce88692a2
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CImage::ReleaseGDIPlus
Releases resources used by GDI+.  
  
## Syntax  
  
```  
  
void ReleaseGDIPlus() throw();  
  
```  
  
## Remarks  
 This method must be called to free resources allocated by a global `CImage` object. See [CImage::CImage](../vs140/CImage--CImage.md).  
  
## Requirements  
 **Header:** atlimage.h  
  
## See Also  
 [CImage Class](../vs140/CImage-Class.md)