---
title: "CImage::IsDIBSection"
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
ms.assetid: 9be37711-be46-42bb-8caa-3b7fe0349ebd
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CImage::IsDIBSection
Determines if the attached bitmap is a DIB section.  
  
## Syntax  
  
```  
  
bool IsDIBSection( ) const throw( );  
  
```  
  
## Return Value  
 **true** if the attached bitmap is a DIB section. Otherwise **false**.  
  
## Remarks  
 If the bitmap is not a DIB section, you cannot use the following `CImage` methods, which support only DIB section bitmaps:  
  
-   [GetBits](../vs140/CImage--GetBits.md)  
  
-   [GetColorTable](../vs140/CImage--GetColorTable.md)  
  
-   [GetMaxColorTableEntries](../vs140/CImage--GetMaxColorTableEntries.md)  
  
-   [GetPitch](../vs140/CImage--GetPitch.md)  
  
-   [GetPixelAddress](../vs140/CImage--GetPixelAddress.md)  
  
-   [IsIndexed](../vs140/CImage--IsIndexed.md)  
  
-   [SetColorTable](../vs140/CImage--SetColorTable.md)  
  
## Requirements  
 **Header:** atlimage.h  
  
## See Also  
 [CImage Class](../vs140/CImage-Class.md)   
 [CImage::Attach](../vs140/CImage--Attach.md)