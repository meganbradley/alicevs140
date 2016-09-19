---
title: "CImage::LoadFromResource"
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
ms.assetid: c5de2e82-ef62-4a4d-b085-b017326bc8d0
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CImage::LoadFromResource
Loads an image from a `BITMAP` resource.  
  
## Syntax  
  
```  
  
      void LoadFromResource(  
   HINSTANCE hInstance,  
   LPCTSTR pszResourceName   
) throw();  
void LoadFromResource(  
   HINSTANCE hInstance,  
   UINT nIDResource   
) throw();  
```  
  
#### Parameters  
 `hInstance`  
 Handle to an instance of the module that contains the image to be loaded.  
  
 `pszResourceName`  
 A pointer to the string containing the name of the resource containing the image to load.  
  
 `nIDResource`  
 The ID of the resource to load.  
  
## Remarks  
 The resource must be of type `BITMAP`.  
  
## Requirements  
 **Header:** atlimage.h  
  
## See Also  
 [CImage Class](../vs140/CImage-Class.md)   
 [CImage::Load](../vs140/CImage--Load.md)