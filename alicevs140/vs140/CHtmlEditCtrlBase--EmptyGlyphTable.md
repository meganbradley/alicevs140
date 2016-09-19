---
title: "CHtmlEditCtrlBase::EmptyGlyphTable"
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
ms.assetid: 38b75504-50b0-4795-b40d-7f8e66386a00
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlEditCtrlBase::EmptyGlyphTable
Removes all entries from the glyph table, which hides all images displayed for tags in design mode.  
  
## Syntax  
  
```  
  
HRESULT EmptyGlyphTable( ) const;  
  
```  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Remarks  
 This method sends the [IDM_EMPTYGLYPHTABLE command ID](https://msdn.microsoft.com/en-us/library/aa769907.aspx) to the WebBrowser control.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlEditCtrlBase Class](../vs140/CHtmlEditCtrlBase-Class.md)   
 [CHtmlEditCtrlBase::AddToGlyphTable](../vs140/CHtmlEditCtrlBase--AddToGlyphTable.md)