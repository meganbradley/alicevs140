---
title: "CImage::GetMaxColorTableEntries"
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
ms.assetid: 2c5cec92-8070-4c6b-b61b-3fe2d75c7f4b
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CImage::GetMaxColorTableEntries
Retrieves the maximum number of entries in the color table.  
  
## Syntax  
  
```  
  
int GetMaxColorTableEntries( ) const throw( );  
  
```  
  
## Return Value  
 The number of entries in the color table.  
  
## Remarks  
 This method supports only DIB section bitmaps.  
  
## Requirements  
 **Header:** atlimage.h  
  
## See Also  
 [CImage Class](../vs140/CImage-Class.md)   
 [CImage::GetColorTable](../vs140/CImage--GetColorTable.md)