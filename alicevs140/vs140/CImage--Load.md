---
title: "CImage::Load"
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
ms.assetid: abf2101c-5b0e-4285-92f2-ed270acc5e3d
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CImage::Load
Loads an image.  
  
## Syntax  
  
```  
  
      HRESULT Load(  
   LPCTSTR pszFileName   
) throw( );  
HRESULT Load(  
   IStream* pStream  
) throw();  
```  
  
#### Parameters  
 `pszFileName`  
 A pointer to a string containing the name of the image file to load.  
  
 `pStream`  
 A pointer to a stream containing the name of the image file to load.  
  
## Return Value  
 A standard `HRESULT`.  
  
## Remarks  
 Loads the image specified by *pszFileName* or `pStream`.  
  
 Valid image types are BMP, GIF, JPEG, PNG, and TIFF.  
  
## Requirements  
 **Header:** atlimage.h  
  
## See Also  
 [CImage Class](../vs140/CImage-Class.md)   
 [CImage::LoadFromResource](../vs140/CImage--LoadFromResource.md)