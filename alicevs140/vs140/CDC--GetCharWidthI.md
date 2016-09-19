---
title: "CDC::GetCharWidthI"
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
ms.assetid: bd75679f-ca62-46dc-b313-861d2ba52c5c
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::GetCharWidthI
Retrieves the widths, in logical coordinates, of consecutive glyph indices in a specified range from the current font.  
  
## Syntax  
  
```  
  
      BOOL GetCharWidthI(  
   UINT giFirst,  
   UINT cgi,  
   LPWORD pgi,  
   LPINT lpBuffer  
) const;  
```  
  
#### Parameters  
 `giFirst`  
 Specifies the first glyph index in the group of consecutive glyph indices from the current font. This parameter is only used if the `pgi` parameter is **NULL**.  
  
 `cgi`  
 Specifies the number of glyph indices.  
  
 `pgi`  
 A pointer to an array containing glyph indices. If the value is **NULL**, the `giFirst` parameter is used instead. The `cgi` parameter specifies the number of glyph indices in this array.  
  
 `lpBuffer`  
 A pointer to a buffer that receives the widths.  
  
## Return Value  
 Nonzero if the function is successful; otherwise 0.  
  
## Remarks  
 This member function emulates the functionality of the function [GetCharWidthI](http://msdn.microsoft.com/library/windows/desktop/dd144864), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::GetCharABCWidths](../vs140/CDC--GetCharABCWidths.md)